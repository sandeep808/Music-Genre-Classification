# Music-Genre-Classification

Extracting music and features Dataset We use GTZAN genre collection dataset for classification.

The dataset consists of 10 genres i.e Blues Classical Country Disco Hiphop Jazz Metal Pop Reggae Rock Each genre contains 100 songs. Total dataset: 1000 songs.

#### Extracting the Spectrogram for every Audio :

A spectrogram is a visual representation of the spectrum of frequencies of a signal as it varies with time. When applied to an audio signal, spectrograms are sometimes
called sonographs, voiceprints, or voicegrams.

#### Extracting features from Spectrogram :

We will extract

Mel-frequency cepstral coefficients (MFCC)(13 in number)

Chroma Frequencies,

rmse,

Spectral Centroid,

Spectral bandwidth,

Spectral Roll-off,

Zero Crossing Rate.

#### Chroma Frequencies:
        Chroma features are an interesting and powerful representation for music audio in which the entire spectrum is projected onto 12 bins representing the 12 distinct semitones (or chroma) of the musical octave. Since, in music, notes exactly one octave apart are perceived as particularly similar, knowing the distribution of chroma even without the absolute frequency (i.e. the original octave) can give useful musical information about the audio -- and may even reveal perceived musical similarity that is not apparent in the original spectra.

#### Spectral Centroid :
        The spectral centroid is commonly associated with the measure of the brightness of a sound. This measure is obtained by evaluating the “center of gravity” using the Fourier transform’s frequency and magnitude information. The individual centroid of a spectral frame is defined as the average frequency weighted by amplitudes, divided by the sum of the amplitudes.

                                    fc = ∑[S(k)*f(k)] / ∑[S(k)]
 
where  S(k)  is the spectral magnitude at frequency bin  k ,  f(k)  is the frequency at bin  k .

#### Spectral bandwidth :
        Bandwidth is the difference between the upper and lower frequencies in a continuous band of frequencies. ... A key characteristic of bandwidth is that any band of a given width can carry the same amount of information, regardless of where that band is located in the frequency spectrum.
librosa.feature.spectral_bandwidth computes the order- p  spectral bandwidth:
        
                                    BW =  ∑ {S(k)[f(k)−fc)]^p)}^(1/p)
 
where S(k) is the spectral magnitude at frequency bin k, f(k) is the frequency at bin k, and fc is the spectral centroid. When p=2, this is like a weighted standard deviation.


#### Spectral Roll-off :
        Spectral rolloff is the frequency below which a specified percentage of the total spectral energy, e.g. 85%, lies.The roll-off frequency is defined as the frequency under which some percentage (cutoff) of the total energy of the spectrum is contained. The roll-off frequency can be used to distinguish between harmonic (below roll-off) and noisy sounds (above roll-off).

#### Zero Crossing Rate :
        The zero-crossing rate is the rate of sign-changes along a signal, i.e., the rate at which the signal changes from positive to zero to negative or from negative to zero to positive.
        
        
        We write the data to a csv file.
