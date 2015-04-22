task :default => :clean

task :clean do
  puts "Cleaning Up LaTeX Workspace"
  sh "rm -f *.aux *.bbl *.blg *.dvi *.log *.pdf *.synctex.gz *.toc"
  sh "rm -f frontmatter/*.aux frontmatter/*.log"
  sh "rm -f mainmatter/*.aux mainmatter/*.log"
end
