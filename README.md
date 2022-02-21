# DiDi-Xi'an dataset for FUFI problem

<details>

<summary> Data source </summary>
  
This dataset is collected by [DiDi Chuxing GAIA Initiative](https://outreach.didichuxing.com/research/opendata), it contains about 1 Bilion trajectories of DiDi drivers in Xi’an, China from October 1 to October 31, 2016. 
</details>

<details>
<summary> ## Data processing </summary>
  
In this dataset, we divide data into training, validation and test set in a ratio of 2 : 1 : 1.
The dataset consists of twoparts, coarse- and fine-grained flow maps, where the coarse- maps are divided into pixel regions of size 32×32 and the fine- maps are divided into size of 128x128.

We collect meteorology factors of Xi'an from [Wold Climate Data](https://en.tutiempo.net) and the weather condition includes 9 categories (e.g., rainy, sunny and cloudy), then we digitize these categories into ordinal values.

We also include humidity and atmospheric pressure data for each flow map. Temperature, wind speed, humidity and pressure are scaled into the range [0, 1] with a min-max linear normalization. 

Time and date factors (e.g., hour of the day, day of the week) are transformed into ordinal values. 
</details>

<summary> ## Dataset description </summary>
  
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


  <summary> Usage </summary>
  
  asdasdasd
  

