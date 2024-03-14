# DSC180-B02
- Jaeda Gantulga (sgantulga@ucsd.edu)
- Jenny Song (jis014@ucsd.edu)
- Matthew Swida (mswida@ucsd.edu)
- Guantong Zhang (g4zhang@ucsd.edu)
- Yoav Freund (yfreund@ucsd.edu)

## Labeling Spectrograms of Audio Data to Detect Changes in Bird Behavior

## About
This project was started by Dr. John Hildebrand of UCSD's own Scripps Institute of Oceanography. The data was collected by Dr. Hildebrand during the COVID-19 pandemic in 2020 by setting microphones around San Diego and recording bird songs as well as other noise in the area. Dr. Hildebrand hopes to build models and present evidence that plane flyovers in San Diego are impacting the behavior of birds in order to cause a policy change around planes in the area. Before that's possible however, audio data needs to be transformed into tabular data.

## How it works
In order to turn audio data into tabular data, we need a way to label the data. These labels can then be used as tabular data to be used for machine learning models. Our labeler is reliant on manuel labeling from human beings, but we have tried to make it as simple as possible. Here is how it works:

- The labeler loads in audio clips one at a time that are all 30 seconds long.
- The person labeling is presented with a spectrogram of the audio clip and the potential labels.
- The person will play the clip and identify noises in the time frame they occur, these noises are visualized on the spectrogram. For each noise they hear they will drag over it on the spectrogram and add the appropriate tag.
- Once this is completed the person hits submit, downloading a JSON file of their labels and the next clip is loaded in.

## What we did
In our first quarter we spent a lot of time working with existing labelers with the hope of being able to have labeled data and start modeling in the second quarter. Unfortunately, none of the labelers we found actually worked, so our project became building a labeler we could use that the greater project team could then use for machine learning models. We found a labeler close to what we needed and adapted it, so that it had the correct labels, could load in new files continuously, and could successfully save labeled files.

## How it will be applied
Eventually a larger team of researchers and graduate students will release this labeler on mechanical turk where people will be paid to create these labels. The labels will be cleaned and used to create deep learning models that assess the noise level of planes and how this affects the behavior and patterns of bird calls. If anything is found, the goal would be to try to change policy around the plane flyovers we hear everyday in San Diego.
