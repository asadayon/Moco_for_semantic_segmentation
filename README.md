# Self-supervised learning of Biofilm images using MoCo
I have utillized the implementation of MoCo by facebook research team to learn the representation of biofilm SEM images for "An AI-based approach for detecting cells and microbial byproducts in low volume scanning electron microscope images of biofilms" paper.
Command line for the main moco:
python3 main_moco.py -a resnet50 --lr 0.03 --batch-size 256 --dist-url 'tcp://localhost:10001' --multiprocessing-distributed --mlp --moco-t 0.2 --aug-plus --cos --world-size 1 --rank 0 [dataset path]

For linear evaluation:
python3 main_lincls.py [data-path] --lr 0.3 --pretrained [model-path]

