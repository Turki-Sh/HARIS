HARIS deploy notes

Assumed live URL:
https://turki-sh.github.io/HARIS/

Files included:
index.html
robots.txt
sitemap.xml
llms.txt
humans.txt
.nojekyll

PowerShell deploy from your local project folder:

cd "C:\Users\Msi\Documents\HARIS Introductory website"
Copy-Item "PATH_TO_EXTRACTED_PACKAGE\index.html" ".\index.html" -Force
Copy-Item "PATH_TO_EXTRACTED_PACKAGE\robots.txt" ".\robots.txt" -Force
Copy-Item "PATH_TO_EXTRACTED_PACKAGE\sitemap.xml" ".\sitemap.xml" -Force
Copy-Item "PATH_TO_EXTRACTED_PACKAGE\llms.txt" ".\llms.txt" -Force
Copy-Item "PATH_TO_EXTRACTED_PACKAGE\humans.txt" ".\humans.txt" -Force
Copy-Item "PATH_TO_EXTRACTED_PACKAGE\.nojekyll" ".\.nojekyll" -Force

git status
git add index.html robots.txt sitemap.xml llms.txt humans.txt .nojekyll
git commit -m "Add SEO and AEO files"
git push

GitHub Pages setup:
Repository Settings
Pages
Source: Deploy from a branch
Branch: main
Folder: / root
Save

If your final GitHub Pages URL is not https://turki-sh.github.io/HARIS/, replace it in index.html, robots.txt, sitemap.xml, llms.txt, and humans.txt before pushing.
