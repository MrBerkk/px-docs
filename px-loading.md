# 🔃​  PX Loading 

Thanks For Purchasing! If you need any help, join our [Discord Support Server](https://discord.gg/AVvkrvrUsW).&#x20;

### :clipboard: Requirements

### 📦 Installation

#### Step 1: Download & Extract

Download the resource and extract it to your `resources` folder.

Recommendation: Rename the downloaded folder to `px-loading`

#### Step 2: Add to Server Config

Add the following line to your `server.cfg`

```
ensure px-loading
```

### Config
```
window.Config = {
    // [GENERAL SETTINGS]
    ServerName: "PIXEL",
    ServerColor: "ROLEPLAY",
    SubTitle: "Welcome to the City",
    SeasonText: "Season 2",
    SeasonStatus: "Live",
    NewsText: "Latest Updates",
    Loading: "Loading...",
    Status: "Status",

    // [BACKGROUND SETTINGS]
    // Choose the background mode.
    // Options: "video", "slider", "image"
    BackgroundType: "video",

    // [IMAGE SETTINGS]
    // Used if BackgroundType is "image" or "slider".
    // 0 = Random Image, 1 = First Image, 2 = Second Image, etc.
    SelectedImage: 0,

    // List of images for "image" or "slider" modes.
    Images: [
        "https://4kwallpapers.com/images/walls/thumbs_3t/10749.jpg",
        "https://4kwallpapers.com/images/walls/thumbs_3t/10829.jpg",
        "https://4kwallpapers.com/images/walls/thumbs_3t/10593.jpg"
    ],

    // [VIDEO SETTINGS]
    // Used if BackgroundType is "video".
    // IMPORTANT: Place your video file inside the 'public/assets/' folder.
    // Example: If your file is 'public/assets/background.mp4', write "./assets/background.mp4".
    VideoFile: "./assets/background.mp4",

    // [THEME COLOR]
    // The main accent color used for buttons, highlights, and progress bars.
    // Use HEX color codes (e.g., #c026d3, #ff0000, #00ff00).
    AccentColor: "#c026d3",

    // [MUSIC PLAYER]
    // Default music volume (0.0 to 1.0).
    MusicVolume: 0.2,
    
    // List of songs to play.
    // You can use remote URLs (http) or local files (assets/song.mp3).
    MusicList: [
        { file: "https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3", name: "Loading Vibes - PX Mix" },
        { file: "https://www.soundhelix.com/examples/mp3/SoundHelix-Song-2.mp3", name: "Chill Step - Night" }
    ],

    // [SOCIAL MEDIA]
    // Links displayed in the news section. Leave empty or remove to hide.
    Discord: "discord.gg/pixelsoft",
    Twitter: "@pixelsoft",
    Website: "https://pixelsoft.tr",

    // [NEWS / ANNOUNCEMENTS]
    // Updates displayed in the middle section.
    // Available colors: "green", "blue", "yellow", "red", "purple"
    News: [
        { tag: "UPDATE", color: "green", title: "Economy Update v2", desc: "Job salaries adjusted." },
        { tag: "EVENT", color: "blue", title: "Weekend Racing", desc: "Saturday 9:00 PM." },
        { tag: "INFO", color: "yellow", title: "Whitelist Apps", desc: "Applications are open." }
    ]
};
```

### :sos:Need Help ?&#x20;

If you encounter any issues during installation or have questions about the script, our support team is ready to help.

Join our community for updates and support: [Click Here to Join Discord](https://discord.gg/AVvkrvrUsW)



Created with ❤️ by PixelSoft