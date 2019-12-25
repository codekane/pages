desc "Builds 316.pdf from current settings"
task :threedots do
  fork { exec('prince  --media=PRINT _site/316/index.html -o "316.pdf" -i html5 --baseurl="http://localhost:4000/"') }
end

desc "Builds dotgrid.pdf from current settings"
task :fourdots do
  fork { exec('prince --media=PRINT _site/dotgrid/index.html -o "dotgrid.pdf" -i -html5 -baseurl="http://localhost:4000/"') }
end
