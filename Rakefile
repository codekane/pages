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

