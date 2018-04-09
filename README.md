# Exoplanet Hunting in Deep Space with Machine Learning

Have you ever wondered if there is life outside of our solar system? I’m sure most of us wondered before about our 
existence and if we are truly alone in space. As a kid, I always was fascinated with space, all the stars, and planets 
and due to my curiosity in cosmology, I decided to use Machine Learning algorithms to investigate a Nasa dataset. 
Let me guide you into a deep learning adventure into space.

![exoplanets](https://user-images.githubusercontent.com/24231101/38481586-60ea1a90-3b80-11e8-8c1c-3d60a4309a73.jpg)

## Do you know what an Exoplanet is?
An Exoplanet (Extrasolar planet) is a planet that exists outside our solar system. Many exoplanets have been discovered over 
the years by Nasa’s Kepler telescope. Scientists discovered a very efficient way to study these occurrences; planets themselves
do not emit light, but the stars that orbit them do. If you study and watch these stars over time there may be a regular 
dimming of their flux (The light intensity). That’s enough evidence to say that there is an orbiting body near the star. 
Further studies of the candidate system capture light at a different wavelength, could solidify the belief or confirm the
existence of these orbiting bodies.

![massachusetts institute of technology nasa gif by mit -source](https://user-images.githubusercontent.com/24231101/38481477-e12cd234-3b7f-11e8-8ba7-0d81121fb937.gif)



In the diagram below, a star is orbited by a blue planet. At t = 1, the starlight intensity drops because it is partially 
obscured by the planet, given our position. The starlight rises back to its original value at t = 2. 
The graph in each box shows the measured flux (light intensity) at each time interval.



My goal was to create a model that can predict the existence of an Exoplanet, utilizing the flux (light intensity) readings from 3198 different stars over time. For this dataset investigation I used Python along with these libraries: Pandas, Jupyter notebook, SKLearn, Numpy, Scipy, Matplotlib and Seaborn. If you want to check the projects requirements or source code, you can find it here.

The Dataset is composed of a test and a training set, containing two different labels, 2 is an exoplanet star and 1 is a non-exoplanet-star.

### Trainset:
5087 rows or observations.
3198 columns or features.
Column 1 is the label vector. Columns 2–3198 are the flux values over time.
37 confirmed exoplanet-stars and 5050 non-exoplanet-stars.
### Testset:
570 rows or observations.
3198 columns or features.
Column 1 is the label vector. Columns 2–3198 are the flux values over time.
5 confirmed exoplanet-stars and 565 non-exoplanet-stars.
![screen shot 2018-04-07 at 7 57 48 pm](https://user-images.githubusercontent.com/24231101/38481614-88e4edcc-3b80-11e8-977f-a33a360f0026.png)

An example of a few the columns and rows.
Issues to note
Initially when I first tried tho create a plot I realized, although the dataset was clean, it was not normalized. So due to that I had to create a function that would do that for me.
![screen shot 2018-04-07 at 8 06 15 pm](https://user-images.githubusercontent.com/24231101/38481613-88c9882a-3b80-11e8-9f1d-9f00af7cc497.png)

![screen shot 2018-04-07 at 8 07 35 pm](https://user-images.githubusercontent.com/24231101/38481612-88b198dc-3b80-11e8-8c85-336eadbd756b.png)



“We do data normalization when seeking for relations. Some people do this methods, unfortunately, in experimental designs. Normalization in experimental designs are meaningless because we can’t compare the mean of, for instance, a treatment with the mean of another treatment logarithmically normalized. In regression and multivariate analysis which the relationships are of interest, however, we can do the normalization to reach a linear, more robust relationship. Commonly when the relationship between two dataset is non-linear we transform data to reach a linear relationship. Here, normalization doesn’t mean normalizing data, it means normalizing residuals by transforming data. So normalization of data implies to normalize residuals using the methods of transformation.”
These are examples of the the light intensity:
![screen shot 2018-04-07 at 8 09 46 pm](https://user-images.githubusercontent.com/24231101/38481611-889a7fbc-3b80-11e8-925c-c4f49c1996bd.png)
![screen shot 2018-04-07 at 8 10 06 pm](https://user-images.githubusercontent.com/24231101/38481610-8881c4fe-3b80-11e8-8511-7bdf864a3250.png)



## Feature Engineering

### Gaussian distribution
In theory the normal distribution is a continuous probability distribution.

“The normal distribution is useful because of the central limit theorem. In its most general form, under some conditions (which include finite variance), it states that averages of samples of observations of random variables independently drawn from independent distributions converge in distribution to the normal, that is, become normally distributed when the number of observations is sufficiently large.”

Example of the Gaussian Histogram
Fourier Transform
When you are dealing with intensity values over time, think of it as different variance frequencies or signals. The Fourier Transformation allows us to decompose the signals into independent frequencies, sample the signals over a period of time (or space) and divide them into their frequency components.



### Linear Regression
Linear approach is for modeling the relationship between a scalar dependent variable y and one or more explanatory variables denoted X.


### Principal Components Analysis (PCA)
The procedure to convert a set of observations of possibly correlated variables into a set of values of linearly uncorrelated variables is called principal components. While analyzing the principle components of this dataset, I notice that the first 10 columns was over 70% of my data.


### K-Means
Is a clustering method of vector quantification. K-Means clustering aims to partition n observations into k clusters in which each observation belongs to the cluster with the nearest mean, serving as a prototype of the cluster.


And after all, I decided to check the light intensity of the exoplanets and non-exoplanets and compare them to each other.


After creating my model and predictions, I was curious to know how long it would take us to eventually get to those exoplanets and compare the speed with the Falcon Heavy. So first I checked the distance between Earth to Mars, but remembered the distance from two planets is constantly changing as they travel around the sun.

“In theory, the closest that Earth and Mars would approach each other would be when Mars is at its closest point to the sun (perihelion) and Earth is at its farthest (aphelion). This would put the planets only 33.9 million miles (54.6 million kilometers) apart. However, this has never happened in recorded history. The closest recorded approach of the two planets occurred in 2003, when they were only 34.8 million miles (56 million km) apart.”

Falcon Heavy is the most powerful operational rocket in the world by a factor of two. With the ability to lift into orbit nearly 64 metric tons (141,000 lb) — -a mass greater than a 737 jetliner loaded with passengers, crew, luggage and fuel — Falcon Heavy can lift more than twice the payload of the next closest operational vehicle, the Delta IV Heavy, at one-third the cost.


If my predictions are correct, it would take us approximately 345 light years to get to these exoplanets.

## Conclusion
I was very surprised with the results of this data exploration; cosmology is one of many passions, and being able to create these predictions was very satisfying. Although this was my final project for my Machine Learning class, I intend to continue exploring beyond my current achievements. Also, Nasa and SpaceX offer many datasets that are fun to explore and I’m excited to see what I will be able to achieve.







