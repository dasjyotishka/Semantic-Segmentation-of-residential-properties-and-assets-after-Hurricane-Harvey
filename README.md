# Semantic-Segmentation-of-residential-properties-and-assets-after-Hurricane-Harvey

## Aim
**Hurricane Harvey** was a devastating [Category 4 hurricane](https://en.wikipedia.org/wiki/Saffir%E2%80%93Simpson_scale) that made landfall on Texas and Louisiana in August 2017, causing catastrophic flooding and more than 100 deaths.  It caused $125 billion in damage, according to the National Hurricane Center. That’s more than any other natural disaster in U.S. history except Hurricane Katrina.

This project was the outcome of a competition hosted at CentraleSupélec to develop performant segmentation models capable of identifying residential property features and neighborhood assets after the major flooding event. The intention was to develop an accurate dense segmentation model for aerial post-flood aerial imagery. High resolution image data of Houston, Texas, USA were provided to participants via GeoEngine.  The provided drone image dataset were utilised in order to train segmentation models to better understand ground conditions after Hurricanes. The goal was to accurately identify and segment common large and small assets in residential Houston after Hurricane Harvey that may or may not be damaged by Hurricane Harvey.

Details of the competition is available at the following [link](https://granular.notion.site/Hurricane-Harvey-Challenge-DSBA-2022-2023-80de810d1f6c4b729c1ee0419cc66943)

## Dataset

The provided Hurricane Harvey dataset contains several hundred drone images of residential neighborhoods in Houston. For each, a dense segmentation mask has been generated for the classes mentioned below. Each mask was further vectorized to provide additional representations for modeling, visualization, and review. 

The datasets were made available at Geoengine in which the competition was hosted. The training images downloaded from the competition website are stored in folder called train_images, and the corresponding masks are stored in a folder called train_masks. Two blank folders are also created in the same directory called test_images. Now, for every item in train_images, it was checked whether its corresponding mask exits in train_mask. If it does not exist, the image was moved from train_images folder to the test_images folder. The post-processed dataset on which the code was run is made available at the following [link](https://drive.google.com/file/d/1bUbz4Qxp_pxENiZd3ZqQpXy-vyzU61S-/view?usp=sharing).

## Results

A DeepLabv3+ based segmentation model with a ResNet-101 encoder and pretrained on Imagenet images was utilised to solve a challenge involving utilisation
of deep learning to perform semantic segmentation on residential properties and assets after Hurricane Harvey. It provided a improved dice-score of 76.25% over
an U-Net model on test dataset on final submission, making it the 4th best model on the leaderboard.
