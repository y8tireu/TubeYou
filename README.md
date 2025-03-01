# How to Fork, Use, and Customize My Video App

This document provides step-by-step instructions on how to fork the repository, use the application locally, and customize it to your liking.

## Table of Contents
1. [Forking the Repository](#forking-the-repository)
2. [Cloning the Repository](#cloning-the-repository)
3. [Project Structure Overview](#project-structure-overview)
4. [Using the Application](#using-the-application)
5. [Customizing the Application](#customizing-the-application)
6. [Deploying Your Customized App](#deploying-your-customized-app)
7. [Additional Customization Tips](#additional-customization-tips)
8. [Support and Contributions](#support-and-contributions)

## Forking the Repository

1. Open your browser and navigate to the GitHub repository:  
   [https://github.com/y8tireu/reponame](https://github.com/y8tireu/reponame)
2. Click the **Fork** button in the top-right corner. This will create a copy of the repository under your GitHub account.

## Cloning the Repository

Once you've forked the repository, clone it to your local machine by running the following commands in your terminal:

```bash
git clone https://github.com/y8tireu/TubeYou/
cd reponame
```

## Project Structure Overview

The repository contains the following files and directories:

```
/project-root
├── index.html        <-- Main application file (self-contained with inline CSS & JavaScript)
├── video.html        <-- Standalone video playback page
├── videos.json       <-- JSON file containing video metadata
├── thumbnails/       <-- Directory for thumbnail images
│     ├── sample.jpg
│     └── another.jpg
└── videos/           <-- Directory for video files
      ├── sample.mp4
      └── another.mp4
```

- **index.html:** The main page where videos are listed, searched, and played.
- **video.html:** A dedicated page for standalone video playback.
- **videos.json:** Contains metadata for each video.
- **thumbnails/** and **videos/**: Directories holding your media assets.

## Using the Application

1. **Run the App Locally:**  
   Open `index.html` in your browser to see the video listing and interface.

2. **Search & Filter:**  
   Use the search bar to filter videos by title, category, or tags.

3. **Video Playback:**  
   Click the **Play** button on any video card to open the video in a new page (`video.html`).

4. **Video Download:**  
   Click the **Download** link to download the video file.

5. **Add Video:**  
   Click the **Add Video** button to be redirected to the GitHub repository if you wish to add more videos or customize further.

## Customizing the Application

### 1. Change the Application Name and Branding

- **Browser Tab Title:**  
  Edit the `<title>` tag in `index.html`.

- **Header Name:**  
  Modify the `<h1>` element within the header section of `index.html` to change the app name.

### 2. Add or Modify Videos

- Open the `videos.json` file.
- Each video is represented by a JSON object. To add a new video, include a new object with the following structure:

```json
{
  "id": "3",
  "title": "New Video Title",
  "description": "Description for the new video.",
  "thumbnail": "thumbnails/new-thumbnail.jpg",
  "videoUrl": "videos/new-video.mp4",
  "category": "CategoryName",
  "tags": ["tag1", "tag2"]
}
```

- Ensure you place the new thumbnail and video files in the respective `thumbnails/` and `videos/` directories.

### 3. Modify the Styles and Layout

- All styles are in the `<style>` section of `index.html`.  
- Adjust colors, fonts, margins, and other CSS properties to match your desired look (e.g., change the dark theme colors or add custom animations).

### 4. Extend Functionality

- **JavaScript:**  
  Enhance the app by editing the inline JavaScript in `index.html` (e.g., add new filtering options, implement pagination, or integrate third-party libraries).

- **HTML:**  
  Add or modify HTML elements to introduce new features or layout changes.

## Deploying Your Customized App

You can deploy your customized application on various platforms:

- **GitHub Pages:**  
  Push your changes to your forked repository and enable GitHub Pages in the repository settings.
  
- **Other Platforms:**  
  Consider using services like Netlify, Vercel, or similar for hosting your static site. Follow their documentation for deployment.

## Additional Customization Tips

- **Custom Fonts:**  
  Incorporate custom fonts by linking to Google Fonts or including your own font files.

- **Responsive Design:**  
  Test your changes on different devices to ensure the interface remains user-friendly across all screen sizes.

- **Advanced Features:**  
  Explore adding user authentication, video commenting, or dynamic video loading if you wish to expand the application's functionality.

## Support and Contributions

- **Issues:**  
  If you encounter any issues or have suggestions, feel free to open an issue on your forked repository.

- **Pull Requests:**  
  Contributions are welcome! If you develop improvements, consider opening a pull request for further review.

Happy coding and enjoy customizing your video app!
