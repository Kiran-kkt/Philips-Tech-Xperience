# Philips-Tech-Xperience
A Classification algorithm trained using a Convolutional Neural Network model on philips dataset to classify images as shaver, smart-baby-bottle, toothbrush and wake-up-light.
This repository delivers the solution to the image classification problem as challenged in the philips case package. Due to the space constraint the docker image has not been uploaded here but, instead a set of instructions are provided to safely download and run docker image successfully.

## Instructions to run the docker image
The docker image has been uploaded to a docker-hub repository.

1. Firstly, make sure that the docker has been installed on your system and up-and-running properly. If incase not, then [follow this link](https://docs.docker.com/install/linux/docker-ce/ubuntu/).
2. Pull the docker image from the docker repository using `~$ docker pull kirankt1995/philips_tech_xperience` command. Incase the docker is run as root, use `sudo` like `~$ sudo docker pull kirankt1995/philips_tech_xperience`.

This docker image comes with all dependency packages installed so there is no need to worry about dependency anxeity :grinning:. An empty folder `/Validation_Images` is also created so one can mount their _test-images-folder_ on host to this folder while running the image in a container.

3. Place all test images in the **_test-images-folder_**. 
4. Now all you have to do is run this command:

`~$ docker run -it --rm -v <src-test_images_dir>:/Validation_Images kirankt1995/philips_tech_xperience:latest python -W ignore classification_model.py`.
 
**Note: Pass in the absolute path in `<src-test_images_dir>` of your _test-images-folder_.**
