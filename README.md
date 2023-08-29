The main file to run the pipeline is Final_int.ipynb.
Final_int.ipynb is a jupyter notebook which has starting of the pipeline, hwrw you can give the input images path.
Next you can select required object detection and text detection models to run.
At first step we have 2 options ,If we choose "S" then Sam model is selected,If we choose "D" then detectron 2 is selected which is retinanet.
At second step we have 2 options, if we choose "M" then MMOCR is selected, If we choose "S" siamese model is selected.
Sam.py contains segment anything model which is one of the object detection model present in the pipeline, here input images are taken and using paramters bbox are made (slices)
detectron 2 contains retinanet model which is one of the object detection model present in the pipeline.
mmocr.py contains mmocr code which is one of the text detection model.
Siamese.py contains siamese code which is used to identify genes and extract them from given input.
Cfg.py contains all the possible settings/configurations which can be changed.
Main_pat_way.py contains the code which splits the genes and relations seperatley by category id. These are predetermined by giving splitting input into 4 categories such as genes,activation , inhabit, none , it also contains postprocessing and it gives results in this format - img_id "file_name" "category_id" "bbox
It also contains gene center where relations code is present.
Body_interface is just used as refernece for Main_pat_way.
Final_int.ipynb contains testing code where we can perform testing on the obtained data by using ground truths to get TF,TP,FP,FN which in turn can be used to calculatge accutracy,precision,f1 score and confusion matrix. With this metrics we can perform blackbox test too.
