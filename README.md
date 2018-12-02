# Signature Recognition

* The entire running of the code is described in this video - https://youtu.be/72gr15LSENw
* More details of the video are described futher

# System requirements
* Python 3
* Numpy 1.14.6
* Tensorflow 1.12.0
* Sklearn 0.18.1
* Matplotlib 2.1.2
* Opencv 3.4.4
* Imutils 0.5.1
* Keras 2.2.4
* PIL 4.0.0

# Dataset

* Dataset - This folder contains the genuine images of 12 users. 10per each. which is used for training the model. These images are similar to the drive link shared by the Axis Bank AI Challenge Competetion but few ids are corrected and modified as they were wrong previously. We highly recommend you to use these datasets only as you may find the Ids issues on drive link shared on Hackerearth page which was recokned as false by most of the participants. (check the discussion page for full proof)

* TestDriveData1 - Contains 10 Genuine signatures of 5 users for testing. (2 images per user) 

* TestDriveData2 -  Contains 10 Forged signatures of 5 users for testing. (2 images per user) 

The capsnet.ipnyb contains the code which is to runned.
On running the code , a separate folder called as the output folder will be created and in this folder the checkpoints and other tensorboard requirements will be stored and updated.
The checkpoints are loaded during the test time for loading the pre-trained variables.

# Running the code
One can simply open the ipython notebook.
Its is suggestible to use the free GPU and TPU provided by google - Google Colaboratory.
Since the model consist of multiplication of rank 4 matrices, it would be suggestible to use a GPU if thr code is run on a local computer.

# Running the Model on Google Colab
Please follow the steps -
1) Clone and save the project locally.
2) Open Google colab and go to file->upload notebook->(upload the CapsNetSignatureModel.ipynb from your local machine).
3) Go to Runtime->changeRuntime->select python 3 and GPU.
4) For Dataset , You can also find it on the clone project 
[ DataSet link - https://drive.google.com/drive/folders/1FclUyojyK8HWSTR2OAosbAnPV0aj1kVm?usp=sharing .] 
5) Download the dataset and Upload it in your Google drive under "Mydrive" (root folder of google-drive).
6) Run the first block and mount the drive on to g-colab.
7) Run the second block and upload the followings files from the cloned project which is saved on your local machine during the cloning process :-
a) hyperparameters.json(application/json) ,
b) logger.py(text/plain) ,
c) model_base.py(text/plain),
d) utils.py(text/plain).
8) Now simply run all the blocks. 
9) The model will train itself till 2700 epochs the stop and run the remaining blocks
10) Check out the value of softmax value of genuine and forged signature that will help to determine the validation capability of the model.
11) If one wants to run the test part of the code , one simply download it the prestored checkpoints from here - https://drive.google.com/drive/folders/1uuMwFN0QwnIiHocE1ropGZq3p6Jz9nKj?usp=sharing
12) The downloaded directory is needed to be put in the same directory as that of the dataset above

(Feel free to change the paths of dataset and the required .py files in the code , depending on where you store them.)

# Running the code on Local Machine
Please follow the steps -
1) Clone the repository at any place on the local machine
```
git clone https://github.com/parth-dedhia/signature_recognition.git
cd signature_recognition
```
2) Now on the teminal open jupyter notebook
3) One can simply run all the code blocks
4) The test images are also provided in the repository but incase if anyone  wants to add new images then one can simply add them in one of the two test directories and run the last few blocks again
5) The otherfiles should not be deleted as they are essential for the code to run
6) If one wants to run the test part of the code , one simply download it the prestored checkpoints from here - https://drive.google.com/drive/folders/1uuMwFN0QwnIiHocE1ropGZq3p6Jz9nKj?usp=sharing
7) The downloaded directory is needed to be put in the same directory as that of the dataset above


# Regex 
FILE STRUCTURE:
1.genuines : genuine signatures of 12 people, 10 sample each.
2.forged : forged signature of the same 12 people as in genuine folder, 10 sample each.

Naming of files : XXXYYZZZ
explaination    XXX - ID number of a person who has done the signature. 
		YY - Image smaple number.
		ZZZ - ID number of person whose signature is in photo. 

for example: 00602023 is an image of signature of person number 023 done by person 006. This is a forged signature.
	     02103021 is an image of signature of person number 021 done by person 021. This is a genuine signature. 

# About the model
* For image recognition , traditionally various flavors of CNN were used , but the recent developments bought by Geoffery Hinton , by his state of the art work in Capsule Network seemed to be more promising in the field of computer vision.
* The complexity of the model is very high , both in terms of time and memory
* The graph shown below , was constructed by the model above.
![alt text](https://github.com/parth-dedhia/signature_recognition/blob/master/Images/graph.png)


# For Further Queries -
 Mail us on -
 meghnani.bhavya@gmail.com ,
 kbgandhi12@gmail.com ,
 prdedhia1998@gmail.com .
