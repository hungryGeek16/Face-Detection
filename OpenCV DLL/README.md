To run:
Open Terminal in the folder which the above files are present and type
python detect_faces.py --image (your image name).(extension) --prototxt deploy.prototxt.txt \
	--model res10_300x300_ssd_iter_140000.caffemodel

for example:
python detect_faces.py --image pic.jpg --prototxt deploy.prototxt.txt \
	--model res10_300x300_ssd_iter_140000.caffemodel
For live detection run:
python detect_faces_video.py --prototxt deploy.prototxt.txt \
	--model res10_300x300_ssd_iter_140000.caffemodel

You can see my outputs in my_outputs folder
