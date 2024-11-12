![GitHub repo size](https://img.shields.io/github/repo-size/codewithsadee/vcard-personal-portfolio)

## Documentation about this project. 

### Step 1: Setting Up Project Repository on GitHub
a. Created a New Repository on GitHub and named it Portfolio-website <br>
b. Clone the repository to my local machine 
```bash
git clone https://github.com/your-username/portfolio-website.git
cd portfolio-website
```
<br>

### Step 2: How I built my Docker image <br>
a. I made use of NGINX for this Static website:
# nginx:alpine (a lightweight web server) to serve this static files.

### Dockerfile

```bash
# Use a lightweight web server to serve static files
FROM nginx:alpine
COPY . /usr/share/nginx/html
EXPOSE 80
```
## NOTE: A Dockerfile is needed to package your application so it can run consistently anywhere.
<br>
b. Testing Locally: I built and ran the Docker image locally to make sure everything works before deploying following the steps below:

### Bash
```bash
docker build -t static-site .
docker run -d -p 8081:80 static-site  # For NGINX
```

### Step 3: GitHub Pages
a. I pushed my Code from the VS code to the main branch after making all my changes:

### Bash
```bash
git add .
git commit -m "Deploying portfolio site"
git push -u origin main --force
```
b. Afterwards, I enabled GitHub Pages to serve your static files on GitHub:
* On my repository on GitHub.
* I navigated to Settings > Pages.
* Under Source, selected the branch (main) and folder (/ (root)) where my static files are located.
* Saved the settings, and GitHub Pages generated a URL for my website.

### Step 4: Challenges I encountered.

* I encountered issues when pushing to GitHub and using the parameter --force worked the magic for me. That is:
```bash
git push -u origin main --force
```


## Demo

![image](https://goodddybag.github.io/Portfolio-website/)


## Contact

If you want to contact me you can reach me at [Twitter](https://www.x.com/Goodybaggggg).

## License

This project is **free to use** and does not contains any license.
