# Video Transcoder

https://bhanu9prakash.github.io/voice-transcoder/

## Overview

**Video Transcoder** is a lightweight web application that allows users to transcode video files directly within their browser. Utilizing modern web technologies and APIs, the application provides an intuitive interface for selecting output codecs, uploading video files via drag-and-drop or file selection, and performing the transcoding process with real-time progress feedback. Once transcoded, users can preview the video and download the output file.

## Features

- **Select Output Codec:** Choose between H.264/AAC (MP4), VP8/Vorbis (WebM), and VP9/Vorbis (WebM) codecs for transcoding.
- **Drag and Drop Upload:** Easily upload video files by dragging them into the designated area or by clicking to open the file selector.
- **Real-Time Progress Bar:** Visual feedback during the transcoding process to monitor progress.
- **Video Preview:** Watch the transcoded video directly within the application.
- **Download Transcoded Video:** Download the resulting video file in the chosen format.
- **Notifications:** Receive visual confirmations when downloads are ready or started.

## Technologies & APIs Used

### 1. **HTML5 & CSS3**
   - **Structure & Styling:** Utilizes semantic HTML5 elements and Tailwind CSS for responsive and modern styling.

### 2. **Tailwind CSS**
   - **Utility-First CSS Framework:** Provides rapid UI development with predefined classes for styling components.

### 3. **JavaScript (ES6+)**
   - **Core Functionality:** Handles user interactions, file processing, and integration with browser APIs.

### 4. **Web APIs**
   
   #### a. **Drag and Drop API**
   - **Purpose:** Enables users to drag and drop video files into the application for uploading.
   - **Implementation:** Listens for `dragover`, `dragleave`, and `drop` events on the drop area to handle file uploads seamlessly.

   #### b. **File API**
   - **Purpose:** Allows the application to read and process files selected by the user.
   - **Implementation:** Accesses the uploaded file through the `File` object and creates object URLs for video playback.

   #### c. **MediaRecorder API**
   - **Purpose:** Facilitates recording of media streams, enabling the transcoding of video files into different codecs.
   - **Implementation:**
     - **Capture Stream:** Uses `video.captureStream()` to obtain a media stream from the uploaded video.
     - **Recording:** Initializes `MediaRecorder` with the selected MIME type (codec) and handles data availability.
     - **Blob Creation:** Compiles recorded chunks into a Blob for video playback and downloading.

   #### d. **URL API**
   - **Purpose:** Creates object URLs for the uploaded and transcoded video files, allowing them to be used as sources for video playback and download links.
   - **Implementation:** Uses `URL.createObjectURL()` to generate URLs for the selected and transcoded videos.

   #### e. **HTMLMediaElement API**
   - **Purpose:** Manages video playback within the application.
   - **Implementation:** Controls video loading, playback, and handling of playback events like `loadedmetadata` and `ended`.

### 5. **Error Handling & User Feedback**
   - **Alerts & Notifications:** Provides users with alerts for errors and notifications for successful actions.
   - **Progress Indicators:** Shows a progress bar during the transcoding process to keep users informed.

## How It Works

1. **Select Output Codec:**
   - Users can choose their desired output codec from a dropdown menu. Options include:
     - H.264/AAC (MP4)
     - VP8/Vorbis (WebM)
     - VP9/Vorbis (WebM)

2. **Upload Video:**
   - Users can either drag and drop a video file into the designated area or click to open the file selector dialog.
   - Once a file is selected, its name is displayed, and the application is ready for transcoding.

3. **Transcode Video:**
   - Upon clicking the "Transcode" button, the application:
     - Validates the selected file and chosen codec.
     - Uses the `MediaRecorder` API to record the video stream in the selected format.
     - Displays a progress bar indicating the transcoding progress.

4. **Preview & Download:**
   - After transcoding, the resulting video is playable within the application.
   - A download link is provided for users to save the transcoded video to their device.

## Setup & Usage

1. **Clone or Download the Repository:**
   ```bash
   git clone https://github.com/your-username/video-transcoder.git
   ```
   *(Replace `your-username` with the actual GitHub username if applicable.)*

2. **Navigate to the Project Directory:**
   ```bash
   cd video-transcoder
   ```

3. **Open the Application:**
   - Simply open the `index.html` file in your preferred web browser.
   - No additional server setup is required as the application runs entirely on the client-side.

4. **Using the Application:**
   - **Select Codec:** Choose your desired output codec from the dropdown.
   - **Upload Video:** Drag and drop a video file into the upload area or click to select a file.
   - **Transcode:** Click the "Transcode" button to begin the process.
   - **Preview & Download:** Once transcoding is complete, preview the video and download it using the provided link.

## Browser Compatibility

The application leverages modern web technologies and APIs. For optimal performance and functionality, it is recommended to use the latest versions of major browsers such as:

- **Google Chrome**
- **Mozilla Firefox**
- **Microsoft Edge**
- **Safari**

**Note:** Some features, especially the `MediaRecorder` API, may have limited support in older browsers. Ensure your browser is up-to-date to experience all functionalities seamlessly.

## Limitations

- **Performance:** Transcoding large video files may be resource-intensive and could lead to performance issues depending on the user's device capabilities.
- **Codec Support:** The availability of certain codecs depends on the browser's support. If a selected codec is not supported, the application will alert the user.
- **Browser Dependencies:** Since the application runs entirely on the client-side, it relies on the browser's implementation of the used APIs. Discrepancies between browsers may affect functionality.

## Future Enhancements

- **Additional Codec Support:** Integrate more codecs to provide users with a wider range of output options.
- **Progress Enhancements:** Provide more detailed progress metrics, such as estimated time remaining.
- **Batch Processing:** Allow users to transcode multiple videos simultaneously.
- **Server-Side Transcoding:** Implement server-side transcoding for handling larger files and reducing client-side resource usage.
- **User Authentication:** Enable user accounts to save transcoding preferences and history.

## Contributing

Contributions are welcome! If you'd like to enhance the application or fix issues, feel free to open a pull request or submit an issue.

1. **Fork the Repository**
2. **Create a Feature Branch**
   ```bash
   git checkout -b feature/YourFeature
   ```
3. **Commit Your Changes**
   ```bash
   git commit -m "Add your feature"
   ```
4. **Push to the Branch**
   ```bash
   git push origin feature/YourFeature
   ```
5. **Open a Pull Request**

## License

This project is licensed under the [MIT License](LICENSE).

## Acknowledgements

- **Tailwind CSS:** For providing a powerful utility-first CSS framework.
- **Modern Web APIs:** Thanks to the developers and communities that maintain the Web APIs leveraged in this application.

---

Feel free to reach out for any questions or suggestions!
