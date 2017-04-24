# Recurrent Scene Parser with Perspective Understanding in the Loop


see [project page](http://www.ics.uci.edu/~skong2/recurrentDepthSeg)


## cityscapes dataset
performance on *valset* [in training, fine-annotated trainset only, flip-augmentation only, one GPU, resnet101 as front-end chunk, softmax loss, multi-scale test]


#### baseline (deeplab with single scale branch)

classes | **`Score Average`** | road | sidewalk | building | wall | fence | pole | traffic light | traffic sign | vegetation | terrain | sky | person | rider | car | truck | bus | train | motorcycle | bicycle
--|--|--|--|--|--|--|--|--|--|--|--|--|--|--|--|--|--|--|--|--
IoU | **`0.738`** | 0.980  |  0.849 |  0.916 | 0.475  | 0.596  | 0.598  | 0.684|  0.780 | 0.918 |  0.619  | 0.941  | 0.803  | 0.594  | 0.939  | 0.631  | 0.759  | 0.621   |  0.562 | 0.755    
nIoU |  **`0.547`** | nan |    nan|     nan|   nan|   nan|   nan|     nan|     nan|    nan|    nan|   nan| 0.635| 0.448| 0.859| 0.398| 0.595| 0.467|  0.396|  0.582

#### baseline + perspective estimation

classes | **`Score Average`** | road | sidewalk | building | wall | fence | pole | traffic light | traffic sign | vegetation | terrain | sky | person | rider | car | truck | bus | train | motorcycle | bicycle
--|--|--|--|--|--|--|--|--|--|--|--|--|--|--|--|--|--|--|--|--
IoU | **`0.748`** | 0.981 | 0.849 | 0.918|0.506 |0.605 |0.604 | 0.67| 0.775| 0.918| 0.627|0.940 |0.804 |0.602 |0.942 |0.679 |0.787 |0.656 | 0.591| 0.753|
nIoU |**`0.556`** |   nan|   nan|   nan|  nan|  nan|  nan|    nan|    nan|   nan|   nan|  nan|0.639|0.460|0.863|0.407|0.612|0.489| 0.398|0.575|


#### baseline + perspective estimation + loop-1
classes | **`Score Average`** | road | sidewalk | building | wall | fence | pole | traffic light | traffic sign | vegetation | terrain | sky | person | rider | car | truck | bus | train | motorcycle | bicycle
--|--|--|--|--|--|--|--|--|--|--|--|--|--|--|--|--|--|--|--|--
IoU | **`0.772`**  |0.983  | 0.859 | 0.925 |0.527  |0.628  |0.640  | 0.703| 0.795 | 0.923 | 0.630  |0.946  |0.816  |0.620  |0.950  |0.748  |0.839  |0.753  | 0.626 | 0.764  |
nIoU | **`0.589`**|   nan|   nan|   nan|  nan|  nan|  nan|    nan|    nan|   nan|   nan|  nan|0.660|0.483|0.869|0.446|0.632|0.572| 0.452| 0.597|



#### ours-loop-2

classes | **`Score Average`** | road | sidewalk | building | wall | fence | pole | traffic light | traffic sign | vegetation | terrain | sky | person | rider | car | truck | bus | train | motorcycle | bicycle
--|--|--|--|--|--|--|--|--|--|--|--|--|--|--|--|--|--|--|--|--
IoU      | **`0.791`** | 0.984     | 0.866     | 0.931      | 0.573      | 0.642     | 0.667 | 0.723   |  0.816       | 0.929     | 0.647      | 0.951     | 0.834    | 0.645      | 0.954    | 0.777      | 0.856    | 0.780     | 0.678     | 0.780 
nIoU | **`0.617`** |     nan|    nan|    nan |    nan |    nan |    nan|  nan|   nan|    nan|    nan |    nan |  0.678|  0.512 |  0.889|  0.476 |  0.666|  0.580|  0.509|  0.624






04/22/2017
Shu Kong @ UCI
