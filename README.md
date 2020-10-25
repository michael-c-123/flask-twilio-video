# What is RoundTable

RoundTable is a video-conferencing website that allows you to place individuals in an arch around you, altering the direction their voice is coming from. This makes it far easier to differentiate between people's voices, especially when multiple people are talking at once.

# Inspiration

Many people, including us, have found ourselves in overcrowded voice or video chats during this unprecedented event for school or meeting with friends and family. It can be difficult to make the most of these calls due to people talking louder and louder over each other to be heard. We thought of a way to solve this: by utilizing the stereo sound features of today's headphones and speakers, we could make voices come from different angles as though people were sitting in an arch around you. This would make it far easier to differentiate between the deluge of voices coming to your ears.

# What it does

RoundTable utilizes the stereo audio system of today's speakers and headphones to position everyone speaking in a call around the user, making it far easier to hear what people are saying when multiple people speak over each other. When you go to RoundTable, you will see your video feed and a place to enter your name and then join the room. Once you do join, you will be placed in the center of an arch of people around you; it will sound as though everyone's voices are coming from their position in this arch. You can then move people around in this arch to change where their voices are coming from, allowing you to position everyone so you can hear them best.

# Core Technologies

 - [Twilio](https://www.twilio.com/)
 - [Flask](https://flask.palletsprojects.com/en/1.1.x/)
 - [JavaScript](https://www.javascript.com/)
 - [HTML](https://html.spec.whatwg.org/)

# Challenges I ran into

Above all else, we faced the challenge of working in a virtual environment with a short time limit. Normally we would all be together in person at the convention center brainstorming ideas and creating our project together, but we had to figure out how to do it all virtually. This shift was a challenge for all of us.

As far as technical challenges, we had many when it came to intercepting the audio streams for each and then changing the direction that audio came from. First we had an issue where, whenever we would log a specific list of HTML elements, it would work correctly but when we attempted to access a specific element, it would not find it. After spending hours trying different fixes to access this element, including busy-waiting to avoid race conditions, and consulting a mentor, we moved the access to earlier in our program before any asynchronous threads could change what we were trying to access.

When we were nearing the finish line with everything working with the video chat, we were implementing the directional audio but could not figure out why our code was not working. After looking at multiple possibilities, including audio contexts and connection issues, we discovered that we were using a static audio stream - one that could not be directionally adjusted. We found the correct function and stream input and finally reached success.

# What I learned

The idea for our project arose from a challenge that our group was determined to tackle. Our project applied front-end web development to create a platform that can solve this problem. During the development process, we learned how to set up and deploy a video call system, use a variety of Web APIs, and present an appealing user interface. We combined our efforts and skills to create a useful and effective project that we are proud to have built.

# What's next for RoundTable

Moving forward, we hope to incorporate RoundTable into other platforms aside from our own, including Discord and Zoom so that our idea can be used by everyone globally. Into RoundTable's own client, we hope to implement another system for positional audio, allowing for people in the room to position themselves in a plane and hear people relative to their location in this plane. We also hope to support additional rooms so that RoundTable is more accessible to all.
