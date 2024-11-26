1、labelimg标注yolo格式：txt文件，每行格式为：类别 x_center y_center width height，其中x_center、y_center、width、height均为浮点数，且值域在0~1之间。</br>
2、创建目录：D:\yolov5\VOCdevkit\VOC2007\Annotations并将标注文件放入Annotations目录和D:\yolov5\VOCdevkit\VOC2007\JPEGImages，并将图片文件放入JPEGImages目录。</br>
3、运行split_train_val.py脚本，将数据集划分为训练集和验证集和测试集，会在ImageSets文件夹下生成4个txt文件。</br>
4、运行voc_label.py脚本，生成训练需要的数据集文件夹images和labels。</br>
5、在data目录下建立自己的my.yaml文件，修改classes和train、val、test的路径。</br>
   * train: D:\yolov5\VOCdevkit\VOC2007\images\train</br>
   * val: D:\yolov5\VOCdevkit\VOC2007\images\val</br>
   * test: D:\yolov5\VOCdevkit\VOC2007\images\test</br>
   * nc: 5  # number of classes</br>
   * names: [qugu, zhigu, shouyaoba, gousuoqijiasuo, zhuanchejiyaoshi]  # class names</br>
6、修改并运行train.py脚本，开始训练。</br>
