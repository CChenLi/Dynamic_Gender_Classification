<img align="right" src="https://user-images.githubusercontent.com/63531857/96329989-b5bf6680-1006-11eb-9d7f-963aba77527b.gif"/>

# Dynamic Gender Classification

- This App takes real-time video captured by camera and makes gender prediction. 
- This is a philosophical model. The model were trained on a generated dataset, where datapoint were meant to approximate the apperance of human, yet applied on real human.


> Acknowledgement:
>> This project relied on the framework developmed by [sayaleepote](https://github.com/sayaleepote)
>> This is Chen Li's first swift Appliction, pure learning purpose. The first picture is a photo of Chen Li, permission of useage authorized.
>> rest of the pictures were randomly collected by Chen Li through Google search. If you are the owner and feel offensed, please contact, and the demo will be replaced ASAP. The project is still under construction, some issues regarding data conversion are yet to be solved, which has affected the accuracy of the model. Most of the problems are due to the fact that *Chen Li* has just started learning of Swift <u>few hours ago</u>. Hopefully, these problems will be resolved soon.



## Build with
- The model was trained on [Microsoft Custom Vision](https://www.customvision.ai/)
- The model was deployed through [CoreML](https://developer.apple.com/documentation/coreml)
- Dataset were provided by [wao.ai](wao.ai)
  - the dataset were 2000 generated image all in the same file, with a csv file to denote label. Unfortunately, Custom Vision doesn't support csv labeling,
  which means Chen Li probablity have to label them by hand or ask his friend to do so.
  - However, Chen Li has taken classk with [Paul Eggert](https://samueli.ucla.edu/people/paul-eggert/), the G.O.A.T., so he wrote a simple bash code to help him
  ```
  #!/usr/bin/env bash
  file="male.csv"
  while IFS= read line
  do
	  cp "$line" male_dir
  done <"$file"   			#which really save Chen's day
  ```
  
## Example from previous static version
<img src="https://user-images.githubusercontent.com/63531857/96330094-75141d00-1007-11eb-887e-835d3cba3e8e.jpg" width="60%">


## Build
- make sure you have xcode toolkit availiable
```
xcode-select --install
```
- get the source code and start build session
```
git clone https://github.com/CChenLi/Dynamic_Gender_Classification
cd Dynamic_Gender_Classification
open ./CustomVisionMicrosoftToCoreML.xcodeproj
```
- select the device or virtual device you gonna build the model
- before click the "play" botton, , make sure add your developer team and sign to trust the projectin `Preference`



