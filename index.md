# Wrist Rehab Device
Replace this text with a brief description (2-3 sentences) of your project. This description should draw the reader in and make them interested in what you've built. You can include what the biggest challenges, takeaways, and triumphs from completing the project were. As you complete your portfolio, remember your audience is less familiar than you are with all that your project entails!

You should comment out all portions of your portfolio that you have not completed yet, as well as any instructions:
```HTML 
<!--- This is an HTML comment in Markdown -->
<!--- Anything between these symbols will not render on the published site -->
```

| **Engineer** | **School** | **Interest** | **Grade** |
|:--:|:--:|:--:|:--:|
| Sasha S | Emerald High School | Biomedical Engineering | Incoming Junior

**Replace the BlueStamp logo below with an image of yourself and your completed project. Follow the guide [here](https://tomcam.github.io/least-github-pages/adding-images-github-pages-site.html) if you need help.**

![Headstone Image](logo.svg)
  
# Final Milestone

**Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.**

<iframe width="560" height="315" src="https://www.youtube.com/embed/F7M7imOVGug" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

For your final milestone, explain the outcome of your project. Key details to include are:
- What you've accomplished since your previous milestone
- What your biggest challenges and triumphs were at BSE
- A summary of key topics you learned about
- What you hope to learn in the future after everything you've learned at BSE



# Second Milestone

<iframe width="560" height="315" src="https://www.youtube.com/embed/y3VAmNlER5Y" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

For my second milestone, I was able to solder all the components on my solderable breadboard, and work on developing better schematics with fritzing. I also updated my code so the green LED flashes when the wrist is in the correct range of motion, and when it goes outside the threshold, the two buzzers go off and the red LED flashes instead. This feedback helps the user quickly adjust their wrist so it is in correct range of motion.

One challenge I faced was figuring out how to apply the Adafruit IMU to my project, since at first I was not getting the readings I expected. I also realized my flex sensor readings were strange because the ground pin was on the same row as the Arduino D10 pin, and once I moved it, it started working better. Another thing that confused me was the IMU, because when it was in the breadboard the serial monitor values were not changing, but when I took it out and kept it wired to the Arduino, the values started changing. After that, I used the code from the Adafruit libraries in the Arduino application and got proper readings, and I was also able to solder the pins onto another Adafruit IMU properly this time. Another challenge I ran into was the breadboard itself, because I changed it to see if there was a faulty connection, but then I realized the new breadboard was split into two halves and the rows were not all connected like I thought. That made wiring a little harder because I had to connect both sides instead of cramming everything onto one half. I also had trouble when stripping the wires because they kept splitting, so I learned I had to use a bigger diameter on the wire stripper to make it easier. What I need to do next is start sewing everything together once I understand how I want to apply the IMU to my project. I also want to add a removable cloth patch to cover the components except for the LEDs, so users can still see the red and green lights while keeping the wires out of the way. Additionally while soldering was I was struggling to figure out where the flex sensor would be best placed. I also sometimes cut the wires too short and had to recut them or change the format or wiring for other components.

<img width="1190" height="439" alt="Screenshot 2026-07-18 at 2 33 16 PM" src="https://github.com/user-attachments/assets/fd5c4d53-8607-47ba-90fa-6a318f1cd72c" />

This is my updated schematic made in Fritzing, which has the actual components I am using unlike Tinkercad. Compared to my last schematic, I had to change the positioning of some components on the Fritzing application, but it did not change anything as everything was going to be soldered onto the solderable breadboard. This helped me because I could better visualize how the components would be wired together since I had the Arduino and Adafruit IMU I was using. transferring everything to another breadboard was important because it was more compact and neat, and it was convinient for the user to have a lighter weight breadboard on their forearm.

<img width="581" height="745" alt="Screenshot 2026-07-17 at 2 40 53 PM" src="https://github.com/user-attachments/assets/420e5265-d3a7-4773-9116-cfeb6eef7c82" /><img width="570" height="675" alt="Screenshot 2026-07-17 at 2 41 34 PM" src="https://github.com/user-attachments/assets/b3462fd5-3494-468a-9dca-d258a2d0fee2" />

I chose to wire on the botton to high the wires, and I also trimmed the pin ends so the used does not feel it poking through the wrist sleeve. 

# First Milestone

<iframe width="560" height="315" src="https://www.youtube.com/embed/GgoyMvBfkQQ?si=PylLuzmM0J2gja_i" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

For my first milestone, I got the main parts of my wrist rehab device wired on the breadboard, including the Arduino Nano ESP32, flex sensor, and two piezo buzzers. I also have code that makes the buzzers beep when the flex sensor bends past a certain angle, so it can detect when the wrist is not in the right position. I was able to solder pins that came with the Adafruit package to the Adafruit component so it could be properly connected on the breadboard, but I had to do it differently since I did not want to damage the small components on the top side, which I would ideally solder on. I chose this project because it has a bioengineering aspect to it, which I found really interesting.

One challenge I faced was understanding the flex sensor readings, because the numbers were really confusing and sometimes I was seeing values in the thousands even when the sensor looked straight, so I had to spend time figuring out how the sensor actually works. Another problem I ran into was with the piezo buzzers, because I tried a few different ones before noticing that the ones that actually worked had the black bottom housing while the broken ones did not. At first I thought removing the “remove after washing” sticker was why they were not working, but that was not the issue since they should still work without it. I also thought the buzzers needed resistors, so I tested them with and without resistors after seeing mixed information online, and confirmed they did not need resistors since, unlike the Arduino Uno which uses 5 volts, I was using the Arduino Nano ESP32, which has 3.3 volts. Another challenge I faced was wiring everything correctly, since I had a single overlapping wire on the breadboard that connected negative to positive, which I did not notice at first. Because of this, nothing was printing in the serial monitor even though everything seemed fine, and after messing around with the wiring I noticed the hidden white wire and resolved that issue. Additionally, the Arduino and breadboard model were slightly different, which was challenging at first, since the power and ground on Tinkercad were on opposite sides of the breadboard I was using, and I was using another Arduino model (Nano ESP32) instead of the default Arduino Uno that Tinkercad provides. This sometimes messed up how the components on the breadboard connected to the Arduino, but I got used to it by understanding and comparing how the pins were located differently. Tinkercad was also missing the Adafruit IMU, which was important for me to add to my breadboard, so I decided to use Fritzing. In the future, I need to explore the Adafruit libraries in the Arduino application to get a better understanding of how I can apply the IMU to my project. A quick change I could add to the code is, instead of simply saying “Bad” when the wrist is flexed or extended at a poor position, it could say “Tilt wrist up/down” so it is more ideal for the user and they get proper feedback.

<img width="935" height="661" alt="Screenshot 2026-07-17 at 8 43 40 AM" src="https://github.com/user-attachments/assets/b30fbdab-2eed-4d67-838e-dd506257bd3f" />
This schematic shows my wrist rehab prototype on the breadboard. The flex sensor is connected to analog pin A0, and the two piezo buzzers are connected to digital pins 6 and 8. I also tested the LED part quickly in Tinkercad, so that part is shown in the diagram even though I did not wire the LEDs on my actual breadboard yet. The resistors for the LED both have a resistance of 100 ohms, but the actual reisisters I am using have a resistance of 120 ohms, and the resistor for my flex sensor is 10k ohms.

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

| **Part** | **Note** | **Price** | **Link** |
|:--:|:--:|:--:|:--:|
| Sewing Kit | Sewing all components on the sleeve | $5.99 | <a href="https://www.amazon.com/Coquimbo-Traveler-Beginner-Emergency-Organizer/dp/B01G3LOLD6/ref=sr_1_7?crid=27CESEBIVTX3Z&keywords=sewing%2Bkit&qid=1689572065&sprefix=sewing%2Bk%2Caps%2C192&sr=8-7&th=1"> Link </a> |
| Piezo Buzzers | Beeps when wrist is out of proper range of motion | $6.99 | <a href="https://www.amazon.com/mxuteuk-Electronic-Computers-Printers-Components/dp/B07VK1GJ9X/ref=sr_1_6?dib=eyJ2IjoiMSJ9.wAyBeRS6gVe44PjVRBtGDNKks-EH_IddvvbrS5lP7ws8lbLh8RNqBaH9kb5xhXhl7MI8WQtio_tKkeH1YD6_yiGX7h2PwsC4Xm4emaporthsw8TqLLYHf3gw3xr_dTGaPUfmfdeCkpORNEhcAxsMfZYgGrRB0yphDoV5bsa_IT1CHUCMRTKJWfTyijyewlOycoYia-zs1sdJNdwYkWur90jqeI909HZS__vONk1Wv9DgVwvs1mk42ujIPDjLdWqpExujHId0l_C_ESKqP2n46A47I6sWRHoHtI9DI8k_ecA.kZsqmeDgDZNGjmc9dBGyjua1olRzvS49-2NieqlP5hI&dib_tag=se&keywords=piezo+buzzer&qid=1719416785&sr=8-6"> Link </a> |
| Flex Sensor | Measures the bending or flexing data | $18.95 | <a href="https://www.sparkfun.com/flex-sensor-4-5.html"> Link </a> |
| Wrist Sleeve | Holds all the flex sensor in place | $19.97 | <a href="https://www.amazon.com/Sparthos-Wrist-Support-Sleeves-Pair/dp/B074CXL9RM/ref=sxin_16_pa_sp_search_thematic-asin_sspa?content-id=amzn1.sym.f5052e1c-21bb-4068-ada8-6befb6325d04%3Aamzn1.sym.f5052e1c-21bb-4068-ada8-6befb6325d04&crid=BSDK6TEHKM0P&cv_ct_cx=wrist%2Bcompression%2Bsleeve&dib=eyJ2IjoiMSJ9.a0DsiZrtl24MGErE3gc3hs-1seJpCWa444LFuc4uL7pQ2OfUK_CsEha6Uf9uNkDHGCFhBOGcesu0YlU33vWUZg.4T09Mf5m41lcN3unhAgnkf-BS-7wLZL42PAvfgzOW1I&dib_tag=se&keywords=wrist%2Bcompression%2Bsleeve&pd_rd_i=B07G4JCSJ7&pd_rd_r=5b8b03e2-eea7-49ee-9e5f-8cbb186e681e&pd_rd_w=S03mj&pd_rd_wg=NPat3&pf_rd_p=f5052e1c-21bb-4068-ada8-6befb6325d04&pf_rd_r=0BBVYDM9P8428SY3RMC3&qid=1719355435&sbo=RZvfv%2F%2FHxDF%2BO5021pAnSA%3D%3D&sprefix=wrist%2Bcompress%2Caps%2C446&sr=1-2-baa1f287-65d3-41a3-a655-8bbba0531537-spons&sp_csd=d2lkZ2V0TmFtZT1zcF9zZWFyY2hfdGhlbWF0aWM&th=1"> Link </a> |
| Adafruit LSM6DS3TR-C + LIS3MDL | Contains gyroscope, accelerometer, and magnetometer | $19.95 | <a href="https://www.adafruit.com/product/5543?gad_source=1&gclid=Cj0KCQjw4MSzBhC8ARIsAPFOuyW3bKrwhMSo2VoSfvSt319uDnnbDld4MoYm0IzXAV2mbivYMjEGez4aApeGEALw_wcB"> Link </a> |
| INIU Portable Charger | Charging my computer | $24.99 | <a href="https://www.amazon.com/INIU-Portable-10000mAh-Accessories-Essentials/dp/B0DP2N5TX7?th=1"> Link </a> |
| Arduino Nano ESP32 | Processor that connects everything and contains code | $19.30 | <a href="https://www.amazon.com/Arduino-ABX00083-Bluetooth-MicroPython-Compatible/dp/B0C947BHK5?th=1"> Link </a> |
| Jumper Wires | Connecting all components on the breadboard | $6.98  | <a href="https://www.amazon.com/Elegoo-EL-CP-004-Multicolored-Breadboard-arduino/dp/B01EV70C78/ref=sr_1_3?crid=1GJIWX8C47LE6&keywords=jumper%2Bwires&qid=1689572180&sprefix=jumper%2Bwire%2Caps%2C200&sr=8-3&th=1"> Link </a> |
| Solderable Breadboard | Connects all soldered components, more convenient to wear on arm | $11.99 | <a href="https://www.amazon.com/Solderable-Breadboard-Electronics-Projects-Gold-Plated/dp/B07YSCGBL7?th=1"> Link </a> |

# Other Resources/Examples
- [Example 1](https://mikulrana.com/Wrist-Rehabilitation-Device/))
- [Example 2](https://www.starlino.com/imu_guide.html#google_vignette))
- [Example 3](https://arneshkumar.github.io/arneshbluestamp/)

# Starter Project - WeevilEye

<iframe width="560" height="315" src="https://www.youtube.com/embed/dgQTHcTxFh4?si=p-jI4gyakN629boF" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

For my first milestone, I chose the Weevil Eye project because it seemed like a good starter project for me since I do not have much background in engineering and I wanted to get used to soldering and building a circuit. The project uses a photocell, resistors, LEDs, and a coin battery, and all of the parts work together so the eyes light up depending on the light level around it. One challenge I faced was where I put too much solder on pins that were too close together, so I had to remove it with a desoldering tool and fix the connection. I also accidentally used the wrong LEDs instead of the red ones I was supposed to use.

Later on I need to make sure the coin battery holder is soldered properly so everything is fully connected and the LEDs can actually light up. With practicing soldering and circuit building, I felt more prepared to move on to my intensive project, the wrist rehabilitation device.
