# DroughtDetectionUsingSatelliteImages
!! Drought Detection using Satellite Imagery and Deep Learning

Dataset Used: We have used LANDSAT8 Satellite Images of Northern Kenya which are in the format of tensorflow records.The current dataset consists of 86,317 train and 10,778 validation satellite images, 65x65 pixels each, in 10 spectrum bands.Human experts (pastoralists) have labeled these with the number of cows that the geographic location at the center of the image could support (0, 1, 2, or 3+ cows).Each pixel represents a 30 meter square, so the images at full size are 1.95 kilometers across. Pastoralists are asked to rate the quality of the area within 20 meters of where they are standing, which corresponds to an area slightly larger a single pixel. Since forage quality is correlated across space, the larger image may be useful for prediction.

Dataset credits: The data used in this research was collected through a research collaboration between the International Livestock Research Institute, Cornell University, and UC San Diego. It was supported by the Atkinson Centre for a Sustainable Future’s Academic Venture Fund, Australian Aid through the AusAID Development Research Awards Scheme Agreement No. 66138, the National Science Foundation (0832782, 1059284, 1522054), and ARO grant W911-NF-14-1-0498.

https://wandb.ai/wandb/droughtwatch/benchmark
https://developers.google.com/earth-engine/datasets/catalog/LANDSAT_LC08_C01_T1_RT

We have preprocessed the dataset by converting the tensorflow data into images by extracting from B4,B3,B2 bands along with their labels. The current dataset distribution has huge imbalance and Even though we tried different methodologies and deep learning models....The recall and accuracy of the classes in multiclassification are very low. To address the above issues, We have balanced the dataset and combined class0,1 into new class0 which is drought class and combined class 1,2 into new class 1 which is no drought class.
Now we have applied different deep learning models to train this data..EfficientNet, basic CNN, VGG16 and MobileNetV2 among all of them EfficientNet has standed out giving the high accuracy.


