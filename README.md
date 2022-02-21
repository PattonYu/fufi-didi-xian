# DiDi-Xi'an dataset for FUFI problem

<details>
  <summary> Paper </summary>
  
  If you find our paper or dataset useful for your research, please cite:
  ```
  @inproceedings{Liang:2019:UIF:3292500.3330646,
   author = {Zhong, Ting and Yu, Haoyang and Li, Rongfan and Xu, Xovee and Luo, Xucheng and Zhou, Fan},
   title = {PROBABILISTIC FINE-GRAINED URBAN FLOW INFERENCE WITH NORMALIZING FLOWS},
   booktitle = {IEEE International Conference on Acoustics, Speech and Signal Processing, ICASSP 2022},
   year = {2022}
} 
  ```
  
</details>

<details>
<summary> Data source </summary>
  
This dataset is collected by [DiDi Chuxing GAIA Initiative](https://outreach.didichuxing.com/research/opendata), it contains about 1 Bilion trajectories of DiDi drivers in Xi’an, China from October 1 to October 31, 2016. 
</details>

<details>
<summary> Data processing </summary>
  
In this dataset, we divide data into training, validation and test set in a ratio of 2 : 1 : 1.
The dataset consists of twoparts, coarse- and fine-grained flow maps, where the coarse- maps are divided into pixel regions of size 32×32 and the fine- maps are divided into size of 128x128.

We collect meteorology factors of Xi'an from [Wold Climate Data](https://en.tutiempo.net) and the weather condition includes 9 categories (e.g., rainy, sunny and cloudy), then we digitize these categories into ordinal values.

We also include humidity and atmospheric pressure data for each flow map. Temperature, wind speed, humidity and pressure are scaled into the range [0, 1] with a min-max linear normalization. 

Time and date factors (e.g., hour of the day, day of the week) are transformed into ordinal values. 
</details>

<details>
<summary> Dataset description </summary>
  
| Dataset              |      DiDi-Xi’an      |
|----------------------|:--------------------:|
| Time range           | 10/1/2016-10/31/2016 |
| Time interval        |      10 minutes      |
| Coarse-grained size  |        32 × 32       |
| Fine-grained size    |       128 × 128      |
| Upscaling factor (N) |           4          |
| Latitude range       |   34.20°N - 34.28°N  |
| Longitude range      |  108.92°E - 109.01°E |
| Temperature/◦C       |      [11.0, 32.0]     |
| Wind speed / mph     |        [0, 9.3]       |
| Weather conditions   |        9 types       |
| Humidity             |      [36%, 100%]      |
| Pressure /hPa        |      [1004, 1026]     |
| Holidays             |           7          |
</details>

<details>
<summary> Usage </summary>

The structure and usage details of the dataset can be refered to [UrbanFM](https://github.com/yoshall/UrbanFM).
  
Unzip train.zip, test.zip, valid.zip into didixian folder, and then move didixian folder to dataset folder of UrbanFM, run the following command:
```
 python -m UrbanFM.train --ext_flag --dataset "didixian"
```
</details>

