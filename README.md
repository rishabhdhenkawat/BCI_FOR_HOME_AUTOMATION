# BCI_FOR_HOME_AUTOMATION

## Abstract 

Brain Computer Interface (BCI) is the direct
connection between the computers and human brain. The BCI
reads the waves produced from the brain at different locations
in the human head, translates these signals into actions and
commands ,that can control the computers. We propose to
integrate this technology with home automation. This
interface system is especially useful for severely disabled or
locked-in individual with no reliable muscular control over
their body parts to interact with surrounded peripherals. The
system involves two parts: an EEG sensor circuit and a Arduino
microcontroller board. The brain waves are captured using
electrodes. These signals are filtered and amplified to remove
noise .These analog signal is converted to digital. The digital
signals are decoded and are used to switch on a device.
Key Words: Brain computer interface, Automation, EEG,
Arduino, Brainwaves

## 1. INTRODUCTION

Amazingly, nothing in the world can be compared with the
human brain. Our Human Brain is highly complex and is
made up of about 100 billion neurons. There are many types
of neurons in our brain such as motor neurons, sensory
neurons. These neurons get fired up while generating a
response for a particular stimulus and generate an electrical
signal. These electrical signals are not fully transferred from
one neuron to another, but some part of it escapes and
reaches the scalp. These signals are captured by the
electrodes and used to control the device.
Home Automation is an area where BCI can be used and our
entire house can be controlled simply by our brain. BCI is a
direct communication pathway between an enhanced or
wired brain and an external device. Braincomputer interface
can be classified into three main groups-invasive, semiinvasive and non- invasive. In invasive BCI systems, the EEG
sensing device are directly placed on human brain through
critical surgery. In semi-invasive BCI system, the EEG
sensing device is placed on our skull, directly on top of
human brain. In non-invasive BCI system, the EEG sensing
device are placed outside our brain and is considered by far
the most practical safest BCI system.
We have proposed a home automation system using BCI in
this paper. Using this technology the life of people would be
further simplified, physical efforts would be considerably
reduced and it would also prove as a boon for physically
disabled people.



## 2. HARDWARE DESIGN

![BLOCK DIAGRAM](https://github.com/rishabhdhenkawat/BCI_FOR_HOME_AUTOMATION/blob/master/brain_controlled_home_automation_block_diagram.jpg)

###### BLOCK DIAGRAM

It has basically an EEG sensor circuit and a
microcontroller.EEG signal is acquired using electrodes. Our
system uses 3 electrode scheme. The electrodes are placed in
3 forehead position. The EEG signal is filtered and amplified
using amplifiers .The filtered and amplified signal is fed to a
microcontroller (Nano board).The microcontroller converts
the analog signal to digital signal. The components used in
our hardware are:
#### A. Electrodes

We will be using dry non-invasive AgCl disposable clinical
electrode. We are using three electrode scheme. These three
electrodes are placed in three particular positions in our
forehead where we will obtain the electrical signals
associated with our eyes.

#### B.IC AD8232

The AD8232 is an integrated signal conditioning block for
ECG and other bio potential measurement applications. It is
designed to extract, amplify, and filter small bio potential
signals in the presence of noisy conditions. This design allows
for an ultra low power analog-to-digital converter or an
embedded micro controller to acquire the output signal
easily. The AD8232 can implement a two-pole high-pass filter
for eliminating motion artifacts and the electrode half-cell
potential. This filter is tightly coupled with the
instrumentation architecture of the amplifier to allow both
large gain and high-pass filtering in a single stage.

#### C. Micro controller

We use ARDUINO UNO board for it’s feasibility and
simplicity. It employs ATMEGA328 microcontroller. It is
programmed in embedded C using Arduino IDE.  The Arduino will do the following
operations:
1. Will take the analog signal data from the ICAD8238 and
process it according to the working specified.
2. The Arduino will send the control signal to the device that
is to be controlled.

![](https://user-images.githubusercontent.com/44580998/72217822-530ddb80-3559-11ea-88d9-e757c181ccc4.PNG)



#### 3. WORKING
Our BCI system captures the electrical signals from the
forehead position. The electrodes will then send the signals
to the amplifier and filter circuit wherein the signal is
amplified and unwanted noise and signals are filtered out
.The analog signals are then converted into digital signals by
the inbuilt ADC of Arduino. Since the electrical signals are
taken from the forehead position near the eyes, they contain
data regarding the eye movement. Thus we obtain the eye
blink count from the obtained electrical signal .The micro
controller process the signals based on the following logic:
1. Whenever we blink, EEG waves will encounter a peak.
2. This peak value is set as threshold value.
3. If we blink, the output of the ADC goes beyond the
threshold value, the Arduino counts it as a blink.
4. The moment we blink, the timer of the microcontroller
will start.
5. If we blink a certain number of times in a certain interval
of time, the micro controller will enable the relay switches.
6. Depending on which relay switch is provided with the
control signal, the respective device turn on.
7. The number of blinks and the interval can be decided by
the user.
As an example, if we blink 2 times in 9 seconds then the relay
one will get the control signal and the device which is
connected to relay 1 will operate.
The above logic can also be implemented using machine
learning, which will greatly reduce the error of the system.
Fig -3: Hardware
#### CONCLUSIONS
It is quite probable that in the future most of our appliances
will be controlled directly through our wishes or the brain
and this project stands as an affirmation to that vision.
Signals from the brain can be further studied and the
technology can be refined to bring about more specific
results. The scope of the project was primarily to establish
control through no physical motion on part of the user and it
has been successful in doing so but it has also laid a
foundation for many applications 
