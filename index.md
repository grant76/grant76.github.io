## Sleep Sound


### Project Topic

The impact of sound on sleep.

### Proposal Abstract 

Most adults require seven to nine hours of sleep a day in order to properly function and be alert the very next day. The problem is that according to the CDC, a third of US adults reported getting less than the recommended amount of sleep. Sleep deprivation is linked to chronic diseases and conditions as well as mistakes both small and large. There are many factors that can lead to sleep deprivation, both internal and external factors, but it is difficult to pinpoint the exact cause. The focus of our project is to tackle a very trivial, but common factor that affects everyone - the environment, more specifically sound. Most people can agree that a silent environment is the best environment to sleep in, but the problem is not every environment can be silent. Environmental noise is tough to block out no matter how quiet or loud it can be, especially if the sound is intermittent, so our focus isn’t to try to block it out, but use it to our advantage instead. Studies have shown that sound machines, like those that produce white noise, help people sleep better by moderating intermittent noise levels and providing a constant source of sound for a more peaceful and well-rested sleep. 

To determine which noise is optimal for sleep we will use a neural network. This network will use data inputs such as noise magnitude and frequency, movement of the individual, and time to fall asleep to track sleep quality.  It will have control over a noise generator to change the types of ambient sound throughout the night.  This data will give us insight into sound’s impact on sleep.

### Machine Learning

For our project we have decided to employ a Long-Short Term Memory (LSTM) neural network.  This architecture falls under the umbrella of Recurrent Neural Networks (RNN).  LTSMs are able to use long-term dependencies to eliminate the memory issues of traditional RNNs [colah].  Long-term memory provides context to the algorithm leading to more accurate outputs compared to other RNNs. This architecture is effective in handling time sequence data (Jeyakumar, Rec 2020 11 02) and thus will pair with our input of a sound signal’s magnitude over time.  The style of LSTM we will be using is the vanilla LSTM as referred to by [Greff, et al., 2017].  It is a baseline that performs well on various data inputs and, with modifications, curtails computational costs and the number of parameters without significant performance loss [Greff, et al., 2017].  These modifications include omitting the peephole connections and connecting the forget gates.  The reductions in run time and data overhead will scale down training time and lead to faster implementation. This is crucial given the short amount of time to finish our project.  There is also plenty of existing code for the LSTMs, such as (Jeyakumar, activity94/Activity-Recognition), (Karpathy, 2015), and (Phi, 2020).  These will be a foundation from which we build and tune our neural network.  

The LSTM will be coded, trained, and validated in Tensorflow using Google Colab.  The training data will include both pre-existing datasets from online sources and sensor data from the microphone on an Arduino Nano 33 Sense.  This microcontroller will also be the platform on which the LSTM will be run once it has been trained.  This will be achieved by converting the Tensorflow code into a Tensorflow Lite model that will be interpreted and loaded onto the Arduino.  The sole input of the model will be a data channel produced by the Arduino’s onboard microphone.  The information in this channel will include the magnitude in decibels of the environment and a timestamp.

The output of our LSTM will be the prediction of the volume of ambient sound in an environment.  This value will be transmitted to a smart phone application that will generate white noise to counteract any sounds that will disturb a sleeping individual.  The magnitude of the white noise will be proportional to the output value of the LSTM.


### Team

Derek Wong and Grant Young

#### References

Jeyakumar, J. V. Rec 2020 11 02. YouTube (2020). Available at: [https://www.youtube.com/watch?v=PKApMIci91Q](https://www.youtube.com/watch?v=PKApMIci91Q). (Accessed: 6th November 2020) 

Jeyakumar, J. V. vikranth94/Activity-Recognition. GitHub (2020). Available at: [https://github.com/vikranth94/Activity-Recognition/blob/master/existing_models.py](https://github.com/vikranth94/Activity-Recognition/blob/master/existing_models.py). (Accessed: 6th November 2020)

Karpathy, A. The Unreasonable Effectiveness of Recurrent Neural Networks (2015). Available at: [http://karpathy.github.io/2015/05/21/rnn-effectiveness/](http://karpathy.github.io/2015/05/21/rnn-effectiveness/). (Accessed: 6th November 2020)

K. Greff, R. K. Srivastava, J. Koutník, B. R. Steunebrink and J. Schmidhuber, "LSTM: A Search Space Odyssey," in IEEE Transactions on Neural Networks and Learning Systems, vol. 28, no. 10, pp. 2222-2232, Oct. 2017, doi: 10.1109/TNNLS.2016.2582924.

Olah, C. Understanding LSTM Networks. Understanding LSTM Networks -- colah's blog (2015). Available at: [https://colah.github.io/posts/2015-08-Understanding-LSTMs/](https://colah.github.io/posts/2015-08-Understanding-LSTMs/). (Accessed: 6th November 2020)

Phi, M. Illustrated Guide to LSTM's and GRU's: A step by step explanation. Medium (2020). Available at: [https://towardsdatascience.com/illustrated-guide-to-lstms-and-gru-s-a-step-by-step-explanation-44e9eb85bf21](https://towardsdatascience.com/illustrated-guide-to-lstms-and-gru-s-a-step-by-step-explanation-44e9eb85bf21). (Accessed: 6th November 2020) 

Jeyakumar, J. V. vikranth94/Activity-Recognition. GitHub (2020). Available at: [https://github.com/vikranth94/Activity-Recognition/blob/master/existing_models.py](https://github.com/vikranth94/Activity-Recognition/blob/master/existing_models.py). (Accessed: 6th November 2020)

Karpathy, A. The Unreasonable Effectiveness of Recurrent Neural Networks (2015). Available at: [http://karpathy.github.io/2015/05/21/rnn-effectiveness/](http://karpathy.github.io/2015/05/21/rnn-effectiveness/). (Accessed: 6th November 2020)

Olah, C. Understanding LSTM Networks. Understanding LSTM Networks -- colah's blog (2015). Available at: [https://colah.github.io/posts/2015-08-Understanding-LSTMs/](https://colah.github.io/posts/2015-08-Understanding-LSTMs/). (Accessed: 6th November 2020)

Phi, M. Illustrated Guide to LSTM's and GRU's: A step by step explanation. Medium (2020). Available at: [https://towardsdatascience.com/illustrated-guide-to-lstms-and-gru-s-a-step-by-step-explanation-44e9eb85bf21](https://towardsdatascience.com/illustrated-guide-to-lstms-and-gru-s-a-step-by-step-explanation-44e9eb85bf21). (Accessed: 6th November 2020) 
