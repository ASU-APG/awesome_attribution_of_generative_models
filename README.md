# Awesome Attribution of Generative Models [![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)
A curated list of resources on attribution of generative models, inspired by [
awesome-implicit-representations ](https://github.com/vsitzmann/awesome-implicit-representations).

Work-in-progress.

This list is intended to introduce the key concepts of attribution of generative models.
We hope that this reading list would be great introduction for whom want to start study this topic. 

We include short summary of paper if necessary.

Note that this list does not include fake detection or fake localization.

## What are attribution of generative models?
Attribution of generative models is a way to trace the source of generated media. 
Existing research mostly focuses on fake detection or fake localization. 
However, attribution of generative models is dealing with not only detection but also classification that maps generated media to the responsible generative model or the owner. 
To achieve stable attribution, the attribution signal should be robust against post-processes (e.g. blur, crop, JPEG compression, etc.). 
Also, this signal needs to be imperceptible to achieve the original goal of the generative model. 
Therefore, attribution methods are evaluated using attribution accuracy, robustness, and imperceptibility.


## What are the threat cases and why attribution is possible solution?
Attribution of Generative Models is motivated by two types of threat models related to the generative models:
1. Malicious Generation <br />
The attackers can create and disseminate generated media for illegal goals (e.g. fake profiles). 
The attribution can help a law enforcement agency to point out suspects.
2. Digital Copyright Infringement <br />
The attackers are the people who download copyrighted digital content (e.g. an art piece created through the assistance of a generative model), makes modification to it, and claims it as their own.
In this case, attribution allows the content owner to protect their intellectual property. 


# Papers
## Model Attribution
The following list of papers showed that the source model of fake media is attributable.
* [Do GANs Leave Artificial Fingerprints?](https://ieeexplore.ieee.org/abstract/document/8695364?casa_token=yTB5X886HvQAAAAA:nIAEKBNZrL07aqIRb6Dml0BHbS-NBSAKiLpn8xzk2YURs0kA2VwE_DkyaadMXRYJkfgssEus) (Marra et al. 2019) examined the artificial fingerprints of GANs can be used for source identification.
* [Source Generator Attribution via Inversion](https://openaccess.thecvf.com/content_CVPRW_2019/papers/Media%20Forensics/Albright_Source_Generator_Attribution_via_Inversion_CVPRW_2019_paper.pdf) (Albright et al.) proposed the method that inverts the given image to find latent vector. 
And this vector is utilized for finding the best reconstruction.
* [Scalable Fine-grained Generated Image Classification Based on Deep Metric Learning](https://arxiv.org/abs/1912.11082) (Xuan et al. 2019)
* [How Do the Hearts of Deep Fakes Beat? Deep Fake Source Detection via Interpreting Residuals with Biological Signals](https://arxiv.org/abs/2008.11363) (Ciftci et al. 2020)
* [Not My Deepfake: Towards Plausible Deniability forMachine-Generated Media](https://arxiv.org/abs/2008.09194) (Zhang et al. 2020)
* [Reverse Engineering of Generative Models: Inferring Model Hyperparameters from Generated Images](https://arxiv.org/abs/2106.07873) (Asnani et al. 2021) proposed a novel problem 'model parsing', which estimates network structure and loss function of open-world fake images. 
* [Learning to Disentangle GAN Fingerprint for Fake Image Attribution](https://arxiv.org/abs/2106.08749) (Yang et al. 2021) proposed GAN Fingerprint Disentangling Network (GFD-Net), which extracts disentangled fingerprint and producing content-irrelevant representation for model attribution. 
## User Attribution 
The following list showed that the users are attributable even if they create fake media using the same structured generative model.
### Sufficient Condition Studies
* [Decentralized Attribution of Generative Models](https://arxiv.org/abs/2010.13974) (Kim et al. 2020) proposed sufficient conditions of user attribution that guarantee a lower bound of attribution.

### Empirical Studies
* [Attributing Fake Images to GANs: Learning and Analyzing GAN Fingerprints](https://openaccess.thecvf.com/content_ICCV_2019/html/Yu_Attributing_Fake_Images_to_GANs_Learning_and_Analyzing_GAN_Fingerprints_ICCV_2019_paper.html) (Yu et al. 2019) introduced a learning-based method to identify the source.
And this work experimentally showed that even the initialization of random seed contributes to the attribution.
* [Artificial GAN Fingerprints: Rooting Deepfake Attribution in Training Data](https://arxiv.org/abs/2007.08457) (Yu et al. 2020) showed that the poisoned training set can be used for the attribution of users.
* [Responsible Disclosure of Generative Models Using Scalable Fingerprinting](https://arxiv.org/abs/2012.08726) (Yu et al. 2020) embeds user attribution into the parameters of GANs. 



## License
License: MIT

