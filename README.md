# The Biomedia ACM Multimedia Sample Submission
This repository aims to provide a skeleton for preparing your submission to the 2019 Biomedia ACM Multimedia Grand Challange. For starters, we require that each submission is delivered in the form of a Docker image. This Docker image should create the submission file described in the challange description. If you are new to docker, a good place to start is the [Get Started](https://docs.docker.com/get-started/) page of the official Docker documentation.

We thank you for your interest in this years Biomedia challange and wish you the best of luck.

## How to Participate
To participate, we require you to build a Docker image of your submission which includes all required dependancies and can be run using the latest version of Docker. Note that the data should not be included within the Docker image itself, as it will be injected by us. Assume that the test dataset will be located at `/biomedia`. An example submission is included within this repository, where we show an example of a Keras based submission.


## Testing your Docker image
To test you submission, run the following bash command:

```bash
sudo docker run -v <test_set_location>:/biomedia -a stdin -a stdout -a stderr <docker_id> > biomedia_submission.txt 
```

The results should be a `.txt` file which lists the name of a file (image or feature) and the assoicated prediction of said file.

## Submitting your Docker Image

To submit your Docmer image, we recommend that you export it using the following bash command:

```bash
sudo docker save <docker_id> > biomedia_image.tar
```

This commadn will produce a tar file of your Docker image which can easily be sent to one of the organizers of Biomedia 2019. Once the Docker image is exported, submit it to one of the following email addresses; steven@simula.no, michael@simula.no or paal@simula.no.