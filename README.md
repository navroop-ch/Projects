**Image convertor to Vangogh Style Painting using ResNet and Unet Transformers

Artistic Image Translation using CycleGAN

Overview
Our project focuses on employing Generative Adversarial Networks (GANs) and the CycleGAN architecture to transform modern photographs into artworks that mirror the distinctive painting style of Vincent Van Gogh. By leveraging datasets sourced from Kaggle, specifically the "Van Gogh Paintings" dataset and the "I’m Something of a Painter Myself" dataset, we aim to bridge historical art with contemporary imagery, creating a unique blend of past and present visual expressions.

Dataset
Van Gogh Paintings

The dataset comprises 308 images of Van Gogh's artwork from folders named 'Aries,' 'Auvers sur Oise,' 'Saint Remy,' and 'Nuenen.'
These folders were selected for their consistent representation of Van Gogh's painted works, distinct from his sketches and drawings.
I’m Something of a Painter Myself

A dataset of 2,000 modern digital images selected from 7,038 available images, providing a diverse range of training examples.
All images in PNG format to simplify data preprocessing, ensuring consistent resolution, color, and size.
Model Architecture
Our model employs the CycleGAN architecture, specifically tailored for unpaired data translation. It consists of the following components:

Model Components

Van Gogh Generator Model (GeneratorP→V): Transforms a Photograph into a Van Gogh-style Painting.
Photograph Generator Model (GeneratorV→P): Transforms a Van Gogh-style Painting into a Photograph.
Van Gogh Discriminator Model (DiscriminatorV): Distinguishes between a generated Van Gogh Painting and a real one.
Photograph Discriminator Model (DiscriminatorP): Distinguishes between a generated photograph and a real one.
Cycle Consistency

Ensures harmonious transformation between real images and generated images in both directions, maintaining consistency and coherence.
Loss Functions

Adversarial Loss: Ensures the generator produces images indistinguishable from real ones.
Cycle Consistency Loss: Maintains consistency between original and transformed images in both forward and backward cycles.
Identity Loss: Ensures the generator returns the input unchanged for identity-preserving transformations.
Model Training
To train the model, we employ backpropagation through both the discriminator and generator, updating weights based on discriminator and generator losses. The adversarial relationship between the generator and discriminator models requires alternate training to achieve optimal results.

Results
U-Net Baseline Model (Example)

Our baseline model, employing a U-Net architecture, demonstrated promising results over 18 epochs. Notably, the generator loss consistently decreased, indicating improved proficiency in creating stylized images. Correspondingly, discriminator losses for both Van Gogh-styled and photographic images showed a downward trend, reflecting the discriminator's increased ability to discern between generated and real images.

Conclusion
Our approach leverages advanced GAN architecture to seamlessly blend historical artistry with contemporary photography, providing a unique tool for artistic expression and exploration. Further experimentation and evaluation with different generator models, such as UNet and ResNet, are detailed in the 'Results' section, providing insights into the effectiveness of each model architecture.
