FROM blang/latex:ubuntu

# Set the working directory to /document
WORKDIR /document

# Copy the current directory contents into the container at /document
COPY ./latex /document

# Install any needed packages specified in requirements.txt
RUN latexmk --pdf main.tex


