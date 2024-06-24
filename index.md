# AI Fitness Band
Allows you to monitor your fitness levels with a tiny, convenient ML-powered fitness band that tracks your activity and provides insights into your health.



| **Engineer** | **School** | **Area of Interest** | **Grade** |
|:--:|:--:|:--:|:--:|
| Daniel W | Lynbrook High | Electrical/Mechanical Engineering | Incoming Junior

<!---**Replace the BlueStamp logo below with an image of yourself and your completed project. Follow the guide [here](https://tomcam.github.io/least-github-pages/adding-images-github-pages-site.html) if you need help.**-->

<img src="David_W.jpg" width="300" height="400">

<>
<!--- 
# Final Milestone


**Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.**

<iframe width="560" height="315" src="https://www.youtube.com/embed/F7M7imOVGug" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

For your final milestone, explain the outcome of your project. Key details to include are:
- What you've accomplished since your previous milestonehttps://www.youtube.com/watch?v=wGviX-kwstI&list=PLe-u_DjFx7etk6dyDuivrw-gQGhkx9TJL&index=51
- What your biggest challenges and triumphs were at BSE
- A summary of key topics you learned about
- What you hope to learn in the future after everything you've learned at BSE



# Second Milestone

**Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.**

<iframe width="560" height="315" src="https://youtu.be/wGviX-kwstI?si=OOS66Woh48r6M3BF" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

For your second milestone, explain what you've worked on since your previous milestone. You can highlight:
- Technical details of what you've accomplished and how they contribute to the final goal
- What has been surprising about the project so far
- Previous challenges you faced that you overcame
- What needs to be completed before your final milestone 
-->
# First Milestone
  To start my project, I showed that I could predict two shoulder movements (lateral raise and chest fly) in real time using Edge Impulse with data from my Arduino Nano 33 BLE Sense.
  
  I connected my Arduino Nano to my computer in order to collect data and link it with Edge Impulse, so that I could then train a model to recognize accelerometer and gyroscope data. I decided to just directly collect data with my Nano connected to the computer via a USB cable for now, and collect more data via Bluetooth later.
  
  I first had to install the proper CLI's, or command line interfaces, for both Edge Impulse and Arduino. This required a lot of troubleshooting over a few days. Since I was using an outdated version of MacOS, I had to use a different version of Homebrew to install everything. Once that was done, I made sure to flash the firmwares for the Edge Impulse CLI and the Arduino CLI, and then it was time to begin the data collecting process.
  
  <img src="Screen Shot 2024-06-24 at 2.19.10 PM.png" >
Figure 1: Above is the impulse design

  Since the Arduino still had to be connected to the computer with a cable, (something to expand upon for my next milestone), I decided to do a few basic shoulder movements and train my model. I had three classes, or movements: lateral raises, chest flies, and a third category called "neither" in which I would do day-to-day movements or not move my arm at all. I then created my impulse using a basic classifier and feature extractor. I made sure to optimize my model to the proper amount of features, as well as fine-tune my data in order to maximize efficiency. 

  <img src="Screen Shot 2024-06-21 at 4.21.45 PM.png" >

  <img src="Screen Shot 2024-06-24 at 2.09.01 PM.png" >
Figure 2: Above is the data before and after filtering, reduces noise and produces a much smoother profile
  
  In the classifier, I made sure to adjust the learning rate and epoch count accordingly, so that my model would minimize loss while learning fast enough. A learning rate is how much the model adjusts, and I needed to change it because it was too small before. Epoch and learning rate are hyperparameters, which determine the model's learning rate and how it adjusts its parameters.
  
  <img src="Screen Shot 2024-06-24 at 2.39.43 PM.png" >
Figure 3: Above is my classifier design, had to decrease learning rate so that it is less sensitive to features since I have a lot, and also increase epoch count so that it learns for longer
  <img src="Screen Shot 2024-06-24 at 2.40.40 PM.png" >
Figure 4: Above is the final deployment, had to make sure to also deploy on the Nano itself

  
  After training, it was time for deployment. I first deployed it on the Arduino IDE, so that I could run it directly from there. The final step was to also deploy it on the Arduino Nano itself, and flash its firmware so that I could also run the model from the terminal directly. The model is now able to predict which movement I'm doing, but is still hindered by the need of a cable. Next up, I'm planning to make both data collection and deployment available via bluetooth. My main challenges during this process were flashing all the necessary firmware, especially during deployment.


# Starter Project

<iframe width="560" height="315" src="https://www.youtube.com/embed/wGviX-kwstI?si=v7bMy-6ZhwkNnDPd" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

I made a basic, calculator for my starter project. This was mainly used for practice with soldering and other basic skills. The calculator itself has the four basic functions and a clear button. During the process, I ended up not using the provided socket and decided to solder the IC in directly, in order to save time as well as give the calculator a sleeker profile. This project succeeded in teaching the basics of soldering and electrical components, and was good preparation for the tasks ahead.

When pressed, the buttons on the circuit board allow the the flow of electricity through resistors, transistors and other components into an integrated circuit, which detects the newfound change in voltage. The IC then runs the input through a series of logic computations in order to compute the intended output, which is then displayed on an LCD screen.

The challenge of this project was the precision required when soldering the components. Some of the pins were very close together, and I would accidentally solder them together, creating a short circuit. Thankfully, I was able to remove the excess solder, and this issue was soon resolved.
<!--
# Schematics 
Here's where you'll put images of your schematics. [Tinkercad](https://www.tinkercad.com/blog/official-guide-to-tinkercad-circuits) and [Fritzing](https://fritzing.org/learning/) are both great resoruces to create professional schematic diagrams, though BSE recommends Tinkercad becuase it can be done easily and for free in the browser. 

# Code
Here's where you'll put your code. The syntax below places it into a block of code. Follow the guide [here]([url](https://www.markdownguide.org/extended-syntax/)) to learn how to customize it to your project needs. 

```c++
void setup() {
  // put your setup code here, to run once:
  Serial.begin(9600);
  Serial.println("Hello World!");
}

void loop() {
  // put your main code here, to run repeatedly:

}
```

# Bill of Materials
Here's where you'll list the parts in your project. To add more rows, just copy and paste the example rows below.
Don't forget to place the link of where to buy each component inside the quotation marks in the corresponding row after href =. Follow the guide [here]([url](https://www.markdownguide.org/extended-syntax/)) to learn how to customize this to your project needs. 

| **Part** | **Note** | **Price** | **Link** |
|:--:|:--:|:--:|:--:|
| Item Name | What the item is used for | $Price | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/"> Link </a> |
| Item Name | What the item is used for | $Price | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/"> Link </a> |
| Item Name | What the item is used for | $Price | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/"> Link </a> |

# Other Resources/Examples
One of the best parts about Github is that you can view how other people set up their own work. Here are some past BSE portfolios that are awesome examples. You can view how they set up their portfolio, and you can view their index.md files to understand how they implemented different portfolio components.
- [Example 1](https://trashytuber.github.io/YimingJiaBlueStamp/)
- [Example 2](https://sviatil0.github.io/Sviatoslav_BSE/)
- [Example 3](https://arneshkumar.github.io/arneshbluestamp/)

To watch the BSE tutorial on how to create a portfolio, click here.
-->
