Convert COCO segmentation annotation to YOLO segmentation format effortlessly with this Python package. The resulting annotations are stored in individual text files, following the YOLO segmentation format convention. 

# COCO to YOLO Segmentation Converter

This repository contains a Python script for converting COCO segmentation annotations to YOLO segmentation format. The YOLO segmentation format is commonly used for training YOLO segmentation models.

## YOLO Segmentation Data Format

The dataset format used for training YOLO segmentation models is as follows:

- One text file per image: Each image in the dataset has a corresponding text file with the same name as the image file and the ".txt" extension.
- One row per object: Each row in the text file corresponds to one object instance in the image.
- Object information per row: Each row contains the following information about the object instance:
  - Object class index: An integer representing the class of the object (e.g., 0 for person, 1 for car, etc.).
  - Object bounding coordinates: The bounding coordinates around the mask area, normalized to be between 0 and 1.

The format for a single row in the segmentation dataset file is as follows: 
`<class-index> <x1> <y1> <x2> <y2> ... <xn> <yn>`

The coordinates are separated by spaces.


## Usage

To use the COCO to YOLO segmentation converter, follow these steps:

1. Clone the repository:
   `git clone https://github.com/z00bean/coco2yolo-seg.git`
3. Prepare your COCO dataset: Modify the COCO annotation JSON file path and specify the desired output folder name in the Python file.
4. Run the conversion script: `python COCO2YOLO-seg.py`

Make sure to replace `path/to/coco_annotations.json` with the actual path to your COCO annotation JSON file and `path/to/output_folder` with the desired output folder path.

The code utilizes the standard Python libraries, json and os, eliminating the need for additional dependencies. Simply provide COCO JSON files as input, and the package will seamlessly convert the dataset annotations into the YOLO segmentation format.

## Contributing

If you find any issues or have suggestions for improvement, feel free to open an issue or submit a pull request. Contributions are welcome!

## License

MIT License.

## References

https://docs.ultralytics.com/datasets/segment

