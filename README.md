PROJECT OVERVIEW

This project presents our solution for the Offroad Autonomy Segmentation Challenge.

We trained a semantic segmentation model using synthetic desert data and evaluated its performance on unseen desert environments. The objective was to maximize IoU score while maintaining good generalization and efficiency.

OBJECTIVE

Train a semantic segmentation model on synthetic desert data

Evaluate performance on unseen test images

Optimize IoU score and inference performance

Document failure cases and improvements

DATASET STRUCTURE

dataset/

train/
    images/
    masks/

val/
    images/
    masks/

testImages/


Classes:

100 - Trees
200 - Lush Bushes
300 - Dry Grass
500 - Dry Bushes
550 - Ground Clutter
600 - Flowers
700 - Logs
800 - Rocks
7100 - Landscape
10000 - Sky

ENVIRONMENT SETUP

Install Anaconda or Miniconda.

Navigate to the ENV_SETUP folder.

Run:

Windows:
setup_env.bat

Mac/Linux:
Create and run setup_env.sh with equivalent commands.

Activate environment:

conda activate EDU

HOW TO TRAIN THE MODEL

Open terminal or Anaconda Prompt.

Navigate to the project directory.

Activate environment:

conda activate EDU

Run training:

python train.py

Training logs and checkpoints will be saved inside the "runs/" directory.

HOW TO TEST THE MODEL

After training is complete:

python test.py

This will:

Generate predictions

Compute IoU score

Output evaluation metrics

REPRODUCING FINAL RESULTS

Ensure dataset is correctly structured.

Activate EDU environment.

Run train.py.

Run test.py.

Compare IoU score with reported benchmark.

PERFORMANCE METRICS

Primary Metric:

IoU (Intersection over Union)

Additional Evaluation:

Training Loss

Validation Loss

Failure Case Analysis

NOTES

Test images were NOT used during training.

Training, validation, and test sets were kept strictly separated.

Model performance depends on hardware (GPU recommended).

Expected inference speed benchmark: < 50ms per image.

SUBMISSION CONTENTS

This repository contains:

train.py

test.py

Configuration files

Model weights

Final Hackathon Report

README.txt

CONTACT & SUPPORT

For issues during development, refer to the hackathon Discord server or official documentation.

END OF FILE
