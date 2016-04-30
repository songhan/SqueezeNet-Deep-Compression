# SqueezeNet-Deep-Compression
This is the 660KB compressed SqueezeNet, which is 363x smaller as AlexNet but has the same accuracy as AlexNet. 

(There is an even smaller version which is only 470KB. It requires some effort to materialize since each weight is 6-bits.)

# Usage

    export CAFFE_ROOT=$your_caffe_root

    python decode.py /ABSOLUTE_PATH_TO/SqueezeNet_deploy.prototxt /ABSOLUTE_PATH_TO/compressed_SqueezeNet.net /ABSOLUTE_PATH_TO/decompressed_SqueezeNet.caffemodel

    note: decompressed_SqueezeNet.caffemodel is the output, can be any name.

    $CAFFE_ROOT/build/tools/caffe test --model=SqueezeNet_trainval.prototxt --weights=decompressed_SqueezeNet.caffemodel --iterations=1000 --gpu 0

# Related SqueezeNet repo 
[SqueezeNet](https://github.com/DeepScale/SqueezeNet)

[SqueezeNet-Deep-Compression](https://github.com/songhan/SqueezeNet-Deep-Compression)

[SqueezeNet-Generator](https://github.com/songhan/SqueezeNet-Generator)

[SqueezeNet-DSD-Training](https://github.com/songhan/SqueezeNet-DSD-Training)

[SqueezeNet-Residual](https://github.com/songhan/SqueezeNet-Residual)

# Related Papers
[SqueezeNet: AlexNet-level accuracy with 50x fewer parameters and< 0.5MB model size](http://arxiv.org/pdf/1602.07360v3.pdf)

[Learning both Weights and Connections for Efficient Neural Network (NIPS'15)](http://arxiv.org/pdf/1506.02626v3.pdf)

[Deep Compression: Compressing Deep Neural Networks with Pruning, Trained Quantization and Huffman Coding (ICLR'16, best paper award)](http://arxiv.org/pdf/1510.00149v5.pdf)

[EIE: Efficient Inference Engine on Compressed Deep Neural Network (ISCA'16)](http://arxiv.org/pdf/1602.01528v1.pdf)

If you find SqueezeNet and Deep Compression useful in your research, please consider citing the paper:

    @article{SqueezeNet,
      title={SqueezeNet: AlexNet-level accuracy with 50x fewer parameters and< 0.5MB model size},
      author={Iandola, Forrest N and Han, Song and Moskewicz, Matthew W and Ashraf, Khalid and Dally, William J and Keutzer, Kurt},
      journal={arXiv preprint arXiv:1602.07360},
      year={2016}
    }

    @article{DeepCompression,
      title={Deep Compression: Compressing Deep Neural Networks with Pruning, Trained Quantization and Huffman Coding},
      author={Han, Song and Mao, Huizi and Dally, William J},
      journal={International Conference on Learning Representations (ICLR)},
      year={2016}
    }

    @inproceedings{han2015learning,
      title={Learning both Weights and Connections for Efficient Neural Network},
      author={Han, Song and Pool, Jeff and Tran, John and Dally, William},
      booktitle={Advances in Neural Information Processing Systems (NIPS)},
      pages={1135--1143},
      year={2015}
    }

    @article{han2016eie,
      title={EIE: Efficient Inference Engine on Compressed Deep Neural Network},
      author={Han, Song and Liu, Xingyu and Mao, Huizi and Pu, Jing and Pedram, Ardavan and Horowitz, Mark A and Dally, William J},
      journal={International Conference on Computer Architecture (ISCA)},
      year={2016}
    }


