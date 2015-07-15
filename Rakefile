task :default => :tex

task :tex => [:clean, :index, :bibliography, :pdf] do
end

task :pdf do
  puts "Creating PDF Document"
  sh "pdflatex main.tex"
  sh "open main.pdf"
end

task :index do
  puts "Creating Index"
  sh "pdflatex main.tex"
  sh "makeindex main"
  sh "pdflatex main.tex"
end

task :bibliography do
  puts "Creating BibTeX Bibliography"
  sh "pdflatex main.tex"
  sh "bibtex main"
  sh "pdflatex main.tex"
end

task :clean do
  puts "Cleaning Up LaTeX Workspace"
  sh "rm -f *.aux *.bbl *.blg *.dvi *.log *.pdf *.synctex.gz"
  sh "rm -f *.idx *.ilg *.ind *.lof *.lot *.toc"
  sh "rm -f frontmatter/*.aux frontmatter/*.log"
  sh "rm -f mainmatter/*.aux mainmatter/*.log"
  sh "rm -f appendix/*.aux appendix/*.log"
end
