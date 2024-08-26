To upload and host a Flutter app on GitHub, you can follow these steps:

### 1. **Initialize Git in Your Project**
   - Open your Flutter project in a terminal.
   - Run the following commands to initialize a new Git repository:

     ```bash
     git init
     git add .
     git commit -m "Initial commit"
     ```

### 2. **Create a New Repository on GitHub**
   - Go to GitHub and log in to your account.
   - Click on the "+" icon in the top-right corner and select "New repository."
   - Give your repository a name and choose to make it public or private.
   - Click "Create repository."

### 3. **Add GitHub Remote and Push Your Code**
   - In your terminal, add the GitHub repository as a remote:

     ```bash
     git remote add origin https://github.com/your-username/your-repository-name.git
     ```

   - Push your code to GitHub:

     ```bash
     git push -u origin master
     ```

### 4. **Host Your Flutter App on GitHub Pages (Optional)**
If you want to host the web version of your Flutter app on GitHub Pages:

   1. **Build the Web App:**
      - Make sure web support is enabled for your Flutter project:

        ```bash
        flutter config --enable-web
        ```

      - Build the web version of your Flutter app:

        ```bash
        flutter build web
        ```

      - The web build files will be generated in the `build/web` directory.

   2. **Create a `gh-pages` Branch:**
      - In your terminal, create a `gh-pages` branch:

        ```bash
        git checkout -b gh-pages
        ```

      - Copy the contents of the `build/web` directory to the root of your repository:

        ```bash
        cp -r build/web/* .
        ```

      - Commit the changes:

        ```bash
        git add .
        git commit -m "Deploy to GitHub Pages"
        ```

      - Push the `gh-pages` branch to GitHub:

        ```bash
        git push -u origin gh-pages
        ```

   3. **Enable GitHub Pages:**
      - Go to your repository on GitHub.
      - Click on "Settings," then scroll down to the "Pages" section.
      - Under "Branch," select `gh-pages` and click "Save."

      After a few minutes, your Flutter web app should be live on GitHub Pages at `https://your-username.github.io/your-repository-name/`.

Now, your Flutter app is both hosted on GitHub and, optionally, available as a web app through GitHub Pages.
