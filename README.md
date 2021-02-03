# EXAMINNER - EXtrAction MusIcal Notes NEtwoRk 
Feature extraction method for the automatic classification of musical genres, based on complex networks and their topological measurements.

## Getting Started
#### Dependencies
You need Python 3.8 or later to use **EXAMINNER - EXtrAction MusIcal Notes NEtwoRk**. You can find it at [python.org](https://www.python.org/).
The follows Python packages are necessaries:
* [librosa](https://librosa.org);
* [igraph](https://igraph.org/);
* [arff](https://pypi.org/project/arff/);
* [pandas](https://pandas.pydata.org/);
* [numpy](https://numpy.org/);

#### Installation
Clone this repo to your local machine using:
```
git clone https://github.com/omatheuspimenta/examinner.git
```
or
```python
pip install examinner
```

## Features
Feature extraction method for the automatic classification of musical genres, based on complex networks and their topological measurements. The measures form a feature vector, which is used to classify its musical genre from the analysis of the structure formed by the musical notes. 


## Example
```python
from examinner import extractor as ex

file_in = "your_file.wav"
duration = 30.0
clip_duration = 3
word = 2
step = 2
class_name = "genre1"
output_name = 'result'
n_threshold = 200
output_format = 'arff'

ex.extractor(file_in=file_in,
			 output_name=output_name,
             class_name=class_name,
             duration=duration,
             clip_duration=clip_duration,
             word=word,
             step=word,
             n_threshold=n_threshold,
             output_format=output_format)
```
## Input and Parameters
|    **Parameters**   | **Type** |                                                    **Description**                                                    |
|:-------------------:|:--------:|:---------------------------------------------------------------------------------------------------------------------:|
|       file_in       |  string  | Input name, for more details [librosa.load](https://librosa.org/doc/latest/generated/librosa.load.html#librosa.load). |
|     output_name     |  string  |                                                   Output file name.                                                   |
|    output_format    |  string  |          Output file format, use 'csv' for .CSV format or use 'arff' to .ARFF format.<br /> **Default: arff**         |
|      class_name     |  string  |                                                  Name of genre music.                                                 |
|    duration (sec)   |  integer |                           Duration to be considered of input music.<br /> **Default: 30.0**                           |
| clip_duration (sec) |  integer |                      Duration of the split to be considered for input music.<br /> **Default: 3**                     |
|         word        |  integer |                  Number of words to be considered for the network construction.<br /> **Default: 2**                  |
|         step        |  integer |                   Number of step to be considered for the network construction.<br /> **Default: 2**                  |
|     n_threshold     |  integer |                            Maximum number for the threshold network.<br /> **Default: 200**                           |



## Output 
**output_name** file which contains the features which was extracted with the **EXAMINER - EXtrAction MusIcal Notes NEtwoRk** procedure.

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## Citation
If you use this software in your work, please cite our paper. (soon)

## License
[MIT](https://choosealicense.com/licenses/mit/)
