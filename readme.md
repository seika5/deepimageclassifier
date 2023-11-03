## Inspiration
Introducing our groundbreaking project: AI-Based Wildlife Protection! Our mission is to safeguard endangered species in their natural habitats using cutting-edge artificial intelligence technology.
## What it does
Identifies movement within camera footage using image subtraction techniques, then submitting frames with movement to the image classification model.  If it is determined that there was an animal inside the frame, it sends a POST request to the FLASK server to store the image.  Finally the database can be viewed through the NextJS frontend.
## How it was built
Animal classifier trained upon the tensorflow inception_v3 model.  Trained upon a dataset of ~4000 images.  Scored Accuracy of ~85% on test dataset
Flask + SQLITE server – stores the images.  Communicates with a RESTful API.
NextJS + Tailwind Frontend – Simple frontend that allows you to easily browse the database.
