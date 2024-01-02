# TireScanAI - An AI app by Diep Nguyen

Video Demo:
--
 
YouTube link: https://www.youtube.com/watch?v=9LM_WB9EAXM

Description:
--

Hi, my name is Diep Nguyen, people also call me Tara. This is my app called TireScanAI. 

I made this app based on my past experience and how it could've helped me when I first got my car. I got a flat tire and didn't know what to do. It took all day to get to know what I needed and believed I spent too much. Throughout this course and learning about coding, I thought about if I could've made something that would've made that day a lot less stressful and cheaper. 

- Just open the app
- take a picture of your tire
- See the information of your tire that you need
- Get a direct google search that shows you how much the tire costs and who offers it.

This app captures a picture with your phone camera and sends it to Google's Vision AI using its API. It then retrieves all text information of the picture. All that text is parsed to only retrieve the identifiable information for the tire, which are width, aspect ratio, and diameter. The results are displayed and a search button becomes available that allows the user to instantly search those tire variables on google, which shows where to buy them from and how much.

For future business versions, I'd like to integrate it to Walmart API or other tire install vendors to only search their inventory.

This would've helped me a lot in the past, but now I hope it can help someone else save time, money, and stress.

File Descriptions:
--

**T3App**: This file is the first interacts when opening the app that directs the app to enter the splash screen rather than the usual default ContentView file.

<strong>SplashscreenView</strong> This file is the first screen that the user sees as soon as they open the app. It then directs to the ContentView file. Creating this file first allowed me to get a sense of the futuristic/blue design of the app.

ContentView: This is the main page where the user interacts with the app. I decided to make this app as easy and intuitive to use so I made the background tire picture the layout of the app where the user can easily know what the app is about and how to start interacting with it by only having a big button that starts the photo capturing process. When the app is opened for the first time, I had to enable the app the ask the user from an iOS system level to allow the app to open the camera app. Once the camera view appears, the user can take the picture of the tire and submit the picture. From here, the app connects to Google's VisionAI through the API and send the picture for the AI to retrienve all the wording on the tire. The end of the code here sends the user to the ResultsView file.

ResultsView: This file opens up the next screen of the results that VisionAI sends back. In the background, without the user seeing, the results are returned. It's a lot of words and numbers that aren't needed so the app parses the wording and singles out width, aspect ratio, and diameter. At first it seems straight forward, but I had to use regex101.com to further breack down the parsing since there were problems capturing the diameter becasue sometimes it captured spaces where it wasn't supposed to. Parsin g code had to be revised to include the first two numbers right after the Ratio to be assigned to Diameter. Once the three fields are captured, they are displayed as well as with an Info bubble that explains to the user what those variables are. Lastly, a button at the bottom will be displayesd to take the user to google shopping to search for that tire size.

Thank you for your time.
