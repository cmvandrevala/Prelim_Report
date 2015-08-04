task :default => :tex

task :tex => [:clean, :index, :glossary, :bibliography, :pdf] do
end

task :pdf do
  puts "Creating PDF Document"
  sh "pdflatex main.tex"
  sh "open main.pdf"
end

task :bibliography do
  puts "Creating BibTeX Bibliography"
  sh "pdflatex main.tex"
  sh "bibtex main"
  sh "pdflatex main.tex"
end

task :glossary do
  puts "Creating Glossary"
  sh "pdflatex main.tex"
  sh "makeindex -s main.ist -o main.gls main.glo"
  sh "pdflatex main.tex"
end

task :index do
  puts "Creating Index"
  sh "pdflatex main.tex"
  sh "makeindex main"
  sh "pdflatex main.tex"
end

task :clean do
  puts "Cleaning Up LaTeX Workspace"
  sh "rm -f *.aux *.bbl *.blg *.dvi *.log *.pdf *.synctex.gz"
  sh "rm -f *.idx *.ilg *.ind *.lof *.lot *.toc *.glo *.gls"
  sh "rm -f *.ist *.nav *.out *.snm"
  sh "rm -f frontmatter/*.aux frontmatter/*.log"
  sh "rm -f mainmatter/*.aux mainmatter/*.log"
  sh "rm -f appendix/*.aux appendix/*.log"
end
