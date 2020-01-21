require 'yaml'
desc "Builds 316.pdf from current settings"
task :threedots do
  fork { exec('prince  --media=PRINT _site/316/index.html -o "316.pdf" -i html5 --baseurl="http://localhost:4000/"') }
end
desc "Builds 316.pdf to printme.pdf file"
task :printme do
  fork { exec('prince  --media=PRINT _site/316/index.html -o "printme.pdf" -i html5 --baseurl="http://localhost:4000/"') }
end

task :prince do
  fork { exec('prince --media=PRINT _site/prince/index.html -o "output.pdf" -i html5 --baseurl="http://localhost:4000/"') }
end

task :index do
  fork { exec('prince --media=PRINT http://localhost:4000/index/ -o "pdf/index.pdf" -i html5 --baseurl="http://localhost:4000/"') }
end

task :cover do
  fork { exec('prince --media=PRINT _site/cover/index.html -o "./assets/pdf/cover.pdf" -i html5 --baseurl="http://localhost:4000/"') }
end

task :reargrid do
  fork { exec('prince --media=PRINT "http://localhost:4000/reargrid/" -o "./assets/pdf/reargrid.pdf" -i html5 --baseurl="http://localhost:4000/"') }
end

task :preset do
  Dir.glob("preset/*.html").each do |ruby|
    name = ruby.gsub(".html", "").gsub("preset/", "")
    fork { exec("prince --media=PRINT http://localhost:4000/#{ruby} -o assets/pdf/#{name}.pdf -i html5 --baseurl='http://localhost:4000/'") }
  end
end

task :predata do
  dataout= []
  Dir.glob("preset/*.html").each do |ruby|
    data = {}
    data[:file] = ruby.prepend("/")
    data[:summary] = ruby.gsub("preset/", "").gsub(".html", "").gsub("/", "")
    data[:pdf] = ruby.gsub(".html", ".pdf").gsub("preset/", "").prepend("/assets/pdf")
    dataout << data
  end
  File.open("_data/predata.yml", "w") { |file| file.write(dataout.to_yaml) }
end
