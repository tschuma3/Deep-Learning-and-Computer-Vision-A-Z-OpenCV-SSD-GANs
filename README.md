# Deep-Learning-and-Computer-Vision-A-Z-OpenCV-SSD-GANs

The Viola-Jones Algorithm
    -- 2 Sections --> Training and Detection
    -- Travels through an image utill it detects a the needed features
    -- The original paper from Viola and Jones --> https://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.10.6807&rep=rep1&type=pdf
Haar-like Features
    -- Derived from the Haar Wave Length
    -- What are they
        -- Edge Features
        -- Line Features
        -- Four-rectangle Features
    -- Paper on the 'General Framework of Object Detection' by Papageorgiou, Oren, and Poggio --> https://www.researchgate.net/publication/3766402_General_framework_for_object_detection
Integral Image
    -- Reduces or minimizes the computational power used
    -- The Idea
        -- For any given value of a square, it is equal to the sum of all square values to the left and above
        -- This allows for the final value to only have to be computes from 4 values
Training Classifiers
    -- When training an AI on facial recognition, it is important to supply images of faces as well as images of non-faces
Adaptive Boosting (Adaboost)
    -- In a 24X24 image, there are on average 180,000 different features (Haar)
    -- F(x) = alpha(of 1) * f(of 1)(x) + alpha(of 2) * f(of 2)(x) + alpha(of 3) * f(of 3)(x) ...
        -- F(x) = Strong Classifier
        -- alpha(of n) * f(of n)(x) = Weak Classifier --> Want to have the most important features first
            -- Each weak feature can complements each other
    -- The idea is that Adaboost will weigh more or make more importance on the incorrect (false positive and false negatives) classifications
Cascading
    -- Intuition
        -- Taking a sub-window and looking at the image to see if a feature is present
            -- No == reject the sub-window
            -- Yes == move on to the next feature
Single Shot Detection (SSD)
    -- Does everything in a single shot with one Convolutional Neural Network
        -- Can deal with training of identifying objects and identifying boarders
        -- Can deal with scaling
    -- The Multi-Box Concept
    -- Predicting Object Positions
    -- The Scale Problem
Generative Adversarial Network (GAN)
    -- Have two components 
        -- Generators (Generative 'G' of GAN)
            -- Create the image and tries to trick the discriminator
        -- Discriminator (Adversarial 'A' of GAN)
            -- Tries and guess what image the generator made
        -- They start from scratch and learn together
        -- Both of them are Networks 'N' of GAN
    -- How the GAN works
        -- The Generator and Discriminator always train together
        -- Input a noise signal into a the Generator
        -- Output the image into the Discriminator along with actual images
        -- Backpropigation occurs and the weights are updated
        -- The Generator updates its weights based on if it has or hasn't tricked the Discriminator
    -- Generative Adversarial Nets by Ian Goodfellow --> https://arxiv.org/pdf/1406.2661.pdf