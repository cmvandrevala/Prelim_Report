task :default => :tex

task :tex => [:clean, :bibliography, :pdf] do
end

task :pdf do
  puts "Creating PDF Document"
  sh "pdflatex main.tex"
  sh "open main.pdf"
end

task :bibliography do
  puts "Creating BibTeX Bibliography"
  sh "latex main.tex"
  sh "bibtex main"
  sh "latex main.tex"
  sh "latex main.tex"
end

task :clean do
  puts "Cleaning Up LaTeX Workspace"
  sh "rm -f *.aux *.bbl *.blg *.dvi *.log *.pdf *.synctex.gz *.toc"
  sh "rm -f frontmatter/*.aux frontmatter/*.log"
  sh "rm -f mainmatter/*.aux mainmatter/*.log"
end
