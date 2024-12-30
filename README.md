Contains the code for a simple microservice for beat detection. Because the installation is a bit complicated and I'd rather not disturb the main repo with it, I've put it in a separate repo. The code is not very clean, but it works. I'll clean it up later, unless I am not bothered enough.

0. Use Python 3.10. Start a new conda env
1. Install ffmpeg
2. pip install spleeter==2.4.0
3. pip install torch torchvision torchaudio --extra-index-url https://download.pytorch.org/whl/cu113
4. pip install Cython==3.0.11 mido==1.3.3
5. git clone --recursive https://github.com/darinchau/madmom.git && mv madmom tmp && mv tmp/* . && rm -rf tmp. If you suspect that the madmom installation is broken, you can install from commit hash 0551aa8, which is known to work
6. python setup.py develop --user
7. git clone --branch=main https://github.com/zhaojw1998/Beat-Transformer
8. pip install uvicorn==0.22.0 fastapi==0.95.1 librosa==0.10.1
9. mv ./Beat-Transformer/code/DilatedTransformer.py ./DilatedTransformer.py
10. mv ./Beat-Transformer/code/DilatedTransformerLayer.py ./DilatedTransformerLayer.py
11. Pray
