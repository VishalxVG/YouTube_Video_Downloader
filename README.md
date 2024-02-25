## YouTube Video Downloader using Pytube

This repository contains a simple YouTube video downloader implemented in Python using the pytube library. It enables users to input a YouTube video URL and downloads the video with the highest available resolution. The downloaded video is then saved in the specified folder.

### How to Use:

1. **Import Necessary Libraries:** Ensure you have the `pytube` library installed for downloading YouTube videos and `tkinter` for creating a graphical user interface (GUI) to get the video URL and save location.

2. **Define the `download_video` Function:** This function takes two arguments: `url` (the YouTube video URL) and `save_path` (the folder where the downloaded video will be saved). Inside the function, a try-except block handles any errors that may occur during the download process.

3. **Create a YouTube Object:** Use the provided URL to create a YouTube object.

4. **Filter Available Streams:** Filter the available streams to get only the progressive (non-adaptive) streams with the "mp4" file extension.

5. **Print Available Streams:** Display the available streams.

6. **Select Highest Resolution Stream:** Get the stream with the highest resolution.

7. **Download Video:** Use the `download` method of the highest resolution stream object to download the video. Save the downloaded video in the specified folder.

8. **Print Success Message:** If the video is downloaded successfully, print a success message.

9. **Define the `open_file_dialog` Function:** This function utilizes the `filedialog` module from `tkinter` to open a file dialog, allowing the user to select a folder for saving the downloaded video.

10. **User Interaction:** In the `__main__` block, initialize the tkinter GUI and hide the window. Prompt the user to input the YouTube video URL and call the `open_file_dialog` function to get the save location.

11. **Download Video:** If a valid save location is provided, download the video using the `download_video` function. If the user cancels the file dialog, print an error message.

12. **Run the Code:** Execute the code. The user will be prompted to enter a YouTube video URL and select a folder to save the downloaded video. The video will then be downloaded and saved in the chosen folder.

### Note:

The pytube library is not actively maintained and may not work with some newer YouTube videos. An alternative approach is to use the `youtube_dl` library, which is more actively maintained and supports a wider range of YouTube videos.

