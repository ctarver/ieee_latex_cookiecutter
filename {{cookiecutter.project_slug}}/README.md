# {{cookiecutter.paper_title}}
Repository for LaTeX for my paper. 
 
## How to compile paper
### Docker

Below is for powershell and windows
```powershell
# Build the new image and compile the documnet
docker build -t paper .
# Spin up a container and get the ID of it
New-Variable -Name id -Value (docker create paper)   
# Copy the main.pdf back 
docker cp ${id}:/document/main.pdf .
docker rm -v $id
Remove-Variable id
```
 
### Normal Linux
 ```bash
cd latex
latexmk --pdf main.pdf
```

 
