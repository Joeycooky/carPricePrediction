# Hotel Booking Prediction : Why people cancel their booking? How can we know if a reservation would be canceled or not? 

This jupyter notebook will guide you through exploratory data analysis, feature engineering and building machine learning model to predict whether a given booking will be canceled or not?

## Install
This project requires **Python 3.x** and the following Python libraries installed:

- [NumPy](http://www.numpy.org/)
- [Pandas](http://pandas.pydata.org)
- [matplotlib](http://matplotlib.org/)
- [scikit-learn](http://scikit-learn.org/stable/)
- [seaborn](https://seaborn.pydata.org/)

You will also need to have software installed to run and execute an [iPython Notebook](http://ipython.org/notebook.html)

We recommend students install [Anaconda](https://www.continuum.io/downloads), a pre-packaged Python distribution that contains all of the necessary libraries and software for this project.

## Introduction
In the present day, booking for a nice, beautiful accommodation are just a click away. 
We can browse through online travel booking platforms, search and made a booking within a minute. 
This benefit not only for traveler like us, but also for hotel operator around the globe. 
<br>
While hotel operator are enjoying benefit from online travel booking platforms to boost their occupancy rate. 
There are also some unavoidable drawbacks, some of them may include higher cancellation rate when online travel booking platforms offer book now pay later promotion.
<br>
Therefore, in order to maximize revenue per room and minimize loss due to cancellation, 
hotel operator should be able to predict whether a given reservation are likely to canceled or not? 
With this information, hotel operator might be able to make an adjustment on overbooking policy during high season to 
compensate for canceled booking. Moreover, they can utilize this information to manage their workforce more effectively.

## Problem Statement

  This could be viewed as supervised binary classification problem. 
  With given booking information : number of guests, number of special requirement, agencies and etc., 
  we will try to predict whether a reservation will be confirmed or canceled.
  <br>
  beside that, I'll try to answer some questions that some of you might have in your mind like...
  
  
* Does lead time has relation with cancellation?
* Which agencies has high rate of cancellation? (rank from top 10 most used agencies)
* What month are likely to be cancelled?
* Which countries are likely to cancel reservation? (rank my top 20 countries)
* If reserved room and assigned room are not the same ? are there any possibility of cancellation?
* Cancellation rate of hotels over period of year
* Which market segment has high rate of cancellation?
* Which distribution channel has high rate of cancellation?

 ## Preliminary Finding
 
>![Distribution](https://github.com/Joeycooky/DataScience-portfolio/blob/master/Hotel%20cancellation%20prediction/image/download.png) 

* Most of booking were made with lead time less than 100 days (approximately 3 months). However we can observe that there are some booking were made in advance with lead time > 400 days 
* Almost all booking were made personally. There are several majors travel agencies involving in making reservation. (From list of more than 500 agencies)

>![Leadtime](https://github.com/Joeycooky/DataScience-portfolio/blob/master/Hotel%20cancellation%20prediction/image/__results___45_0.png)

It has been observed that
* Guest who not canceled the reservation often have short lead time.
* Guest with high amount of special request seem to have interest in hotel and have less cancellations than guest without special request
* Guest with some booking change (1-5) has lower possibility of cancellations than one who doesn't make any change
* Guest who demands single parking space has no cancellations!

## Conclusion

We have explored the data and able to extracted some useful insights since exploratory data analysis. We’ve found that the booking are likely to be canceled if ... 
* they have incredibly long lead time, 
* have little or no special requirements, 
* booked with full broad meal ,etc. 

Some specific group of guests also have higher chance of cancellation than the others. For example, guests from Portugal themselves has higher rate of cancellation than some foreign travelers .

Moreover, we have trained classification models to predict whether a given reservations will be canceled or not. The outcome of the model quite satisfy (with an accuracy of 89.2%). Although it can be improved by training with more data and adjusting regularization parameters. But with current performance, our model has shown significant improvement from benchmark which can be utilized to adjust overbooking policy to achieve higher occupancy rate. In addition, even low season period when booking amount doesn’t fulfill hotel capacity. The model can be used to manage hotel workforce according to fluctuation in demand in each period of years.


## You can find more detail in notebook [here](https://nbviewer.jupyter.org/github/Joeycooky/DataScience-portfolio/blob/master/Hotel%20cancellation%20prediction/hotel-demand.ipynb)
## Notes
This notebook for self-learning purpose only
