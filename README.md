## Functions Introduction
    python main.py --help
    
    usage: main.py [-h] [--image] [--input [INPUT]] [--output [OUTPUT]]
                   [--cam [CAM]] [--web [WEB]] [--online [ONLINE]] [--rtsp [RTSP]]
    
    optional arguments:
      -h, --help         show this help message and exit
      --image            Image detection mode, will ignore all positional
                         arguments, press Ctrl+C to stop.
      --input [INPUT]    [Optional] Video input path
      --output [OUTPUT]  [Optional] Video output path
      --cam 	         [Optional] Using camera,by default using built-in camera
                         of laptop,press Esc to stop.
      --web              [Optional] Using web server,press Ctrl+C to stop.
      --online           [Optional] Using a C/S structure system, will start a
                         video stream detecting client. Please run remote.py on
                         the device with a camera and configure ip and port in
                         settings.py first. Press Esc to stop.
      --rtsp [RTSP]      [Optional] Detect video stream from an IP camera or
                         something else. Need rtsp address as an argument.
            
remote_server.py can start an online streaming server which sends local camera's video stream to client.
                         
## Performance Test
With little time ,energy and money to test its performance, further tests are welcomed for this project and you can merge your test results branch into mine in any time.
## Training Instrction
Files under tool/ are used to train your own dataset. Considering about that different datasets have different formats of annotations, there are only specific training instructions for VOC dataset.For VisDrone2018 Daataset, tools in tool folder will help.

1.Make sure that there is a VOC2007 format dataset folder named VOCdevkit.

2.If classes you need are NOT in pre-trained weights, training without weights is your best choice. For training without pre-trained weights, train_barely.py suits your requirements.Adjust epoch and batch_size according to your hardware situation. Too large batch_size could lead to out of memory and too many epoches cause model you train has no robustness.

3.If classes you need are IN pre-trained weights, please use train.py.

## Model Download
For the offical model training on VOC dataset: https://pjreddie.com/media/files/yolov3.weights

For my model training on VisDrone dataset: 
https://pan.baidu.com/s/1vhSEPMckC7QogL1WdOjWVQ Code：ouvo
OR
https://drive.google.com/file/d/1UT_l0BkBTKZBT4wDqmFf4dU22fPz8g3K/view?usp=sharing

For my training dataset: (BaiduNetdisk)https://pan.baidu.com/s/1QTzy8S7IHSHWtkrFxd100w Code: kdfv

Considering the requirements of the Competition, I prefer to use VisDrone2018 Dataset instead of VOC Dataset. 
