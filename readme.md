## Inspiration
Introducing our groundbreaking project: AI-Based Wildlife Protection! Our mission is to safeguard endangered species in their natural habitats using cutting-edge artificial intelligence technology.
## What it does
Identifies movement within camera footage using image subtraction techniques, then submitting frames with movement to the image classification model.  If it is determined that there was an animal inside the frame, it sends a POST request to the FLASK server to store the image.  Finally the database can be viewed through the NextJS frontend.
## How we built it
Animal classifier trained upon the tensorflow inception_v3 model.  Trained upon a dataset of ~4000 images.  Scored Accuracy of ~85% on test dataset
Flask + SQLITE server – stores the images.  Communicates with a RESTful API.
NextJS + Tailwind Frontend – Simple frontend that allows you to easily browse the database.
## Challenges we ran into
We faced many issues trying different types of AI models.  We looked into models like ResNet, MobileNet, etc, but couldn't implement / train them how we wanted.  We wanted to also run this on an NVIDIA Jetson NANO, but struggled with the implementation as a result of dependency / version issues. 
## Accomplishments that we're proud of
Image subtraction, decently high accuracy image classification, connected fullstack application.
## What we learned
Tensorflow, how to train models, FLASK, object detection.
## What's next for WildEyeAI
More extensive frontend
Accuracy could be improved with better models – MobileNet-SSD / other object classifiers built specifically for video.
More data to be trained on / video data.  Frames in VideoData for MobileNet need to be individually classified so we didn't have time for that during this hackathon.
Image classification can also be improved if we had more categories.  
The model struggles with identification of stuff that it isn't trained on, which makes sense.  We tried mitigating this by training it on blank backgrounds which did vastly improve its capabilities, but stuff like MobileNetSSD -- trained on a much larger dataset -- would do a lot better.
