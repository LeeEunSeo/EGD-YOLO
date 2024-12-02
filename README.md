# EGD-YOLO

python train_aux.py --workers 8 --device 0 --batch-size 16 --data data/egd.yaml --img 1280 1280 --cfg cfg/training/yolov7-w6.yaml --weights 'yolov7-w6_training.pt' --name yolov7-w6 --hyp data/hyp.scratch.p6.yaml </br></br>
python train_aux.py --workers 8 --device 0 --epochs 100 --batch-size 16 --data data/egd.yaml --img 640 640 --cfg cfg/training/yolov7-w6.yaml --weights 'yolov7-w6_training.pt' --name yolov7-w6 --hyp data/hyp.scratch.p6.yaml </br></br>
python train_aux.py --workers 8 --device 0 --epochs 1000 --batch-size 16 --data data/egd.yaml --img 640 640 --cfg cfg/training/yolov7-w6.yaml --weights 'yolov7-w6_training.pt' --name yolov7-w6 --hyp data/hyp.scratch.p6.yaml </br></br>


tensorboard --logdir runs/train </br></br>

python test.py --data data/egd.yaml --img 640 --batch 16 --conf 0.001 --iou 0.65 --device 0 --weights runs/train/yolov7-w634/weights/best_870.pt --name yolov7_634_val </br></br>
