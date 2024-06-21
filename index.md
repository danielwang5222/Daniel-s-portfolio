# AI Fitness Band
Allows you to monitor your fitness levels with a tiny, convenient ML-powered fitness band that tracks your activity and provides insights into your health.



| **Engineer** | **School** | **Area of Interest** | **Grade** |
|:--:|:--:|:--:|:--:|
| Daniel W | Lynbrook High | Electrical/Mechanical Engineering | Incoming Junior

<!---**Replace the BlueStamp logo below with an image of yourself and your completed project. Follow the guide [here](https://tomcam.github.io/least-github-pages/adding-images-github-pages-site.html) if you need help.**

<!---![Headstone Image](logo.svg)-->
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
# First Milestone-->

To start my project, I had to connect my arduino to my computer in order to collect data using edge impulse. Originally, I was planning to collect data via a custom python script that would use BLEAK to link to edge impulse directly. However, seeing as how this was very time-consuming and I was already in over my head, I decided to save that idea for my second milestone. I decided to just directly collect data with my nano connected to the computer via a USB cable for now, and collect more data via bluetooth later.

I first had to install the proper CLI's for both edge impulse and arduino, which proved to require a lot of troubleshooting over the next few days. Once that was done, I made sure to flash the firmware, and then it was time to begin the data collecting process.

Since the arduino still had to be connected to the computer with a cable, (something I will fixt next milestone), I decided to do a few basic shoulder movements and train my model to around an 80% accuracy. I had three classes, or movements: lateral raises, chest flies, and a third category called "neither" in which I would do day-to-day movements or not move my arm at all. I then created my impulse using a basic classifier and feature extractor. I made sure to optimize my model to the proper amount of features, as well as fine-tune my data in order to maximize efficiency. In the classifier, I made sure to adjust the learning rate and epoch count accordingly, so that my model would minimize loss while learning fast enough.

After training, I then deployed my model in both the arduino IDE and on the nano itself. The model is now able to predict which movement I'm doing, but is still hindered by the need of a cable. Next up, I'm planning to make both data collection and deployment available via bluetooth. My main challenges during this process were flashing all the necessary firmware, especially during deployment.
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
