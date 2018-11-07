###  conda install tensorflow-gpu

---

- 英文来源：
  - [https://www.anaconda.com/blog/developer-blog/tensorflow-in-anaconda/](https://www.anaconda.com/blog/developer-blog/tensorflow-in-anaconda/)
  - [https://towardsdatascience.com/stop-installing-tensorflow-using-pip-for-performance-sake-5854f9d9eb0c](https://towardsdatascience.com/stop-installing-tensorflow-using-pip-for-performance-sake-5854f9d9eb0c)


- 翻译来源：
  - [https://littleostar-blog.github.io/-conda-install-tensorflow-gpu-on-windows-10/](https://littleostar-blog.github.io/-conda-install-tensorflow-gpu-on-windows-10/)

---

- Tensorflow in Anaconda (Friday, September 7th 2018)

    By Jonathan Helmus

    TensorFlow是一个用于高性能数值计算的Python库，允许用户创建复杂的深度学习和机器学习应用程序。 TensorFlow于2015年作为开源软件发布，在数据科学界取得了巨大的发展和普及。

    有许多方法可用于安装TensorFlow，例如使用pip来安装PyPI上可用的轮子。使用conda软件包安装TensorFlow具有许多优点，包括完整的软件包管理系统，更广泛的平台支持，更加简化的GPU体验以及更好的CPU性能。这些软件包可以通过Anaconda Repository获得，安装它们就像从命令行界面运行“conda install tensorflow”或“conda install tensorflow-gpu”一样简单。

    使用conda而不是pip安装TensorFlow的一个主要好处是conda包管理系统的结果。当使用conda安装TensorFlow时，conda也会为包安装所有必需和兼容的依赖项。这是自动完成的;用户无需通过系统软件包管理器或其他方式安装任何其他软件。此外，Anaconda存储库中1,400多个专业构建的软件包中的任何一个都可以与TensorFlow一起安装，以提供完整的数据科学环境。这些软件包安装在隔离的conda环境中，其内容不会影响其他环境。

    与Anaconda存储库中的其他软件包一样，TensorFlow在许多平台上都受支持。 TensorFlow conda软件包适用于Windows，Linux和macOS。 1.10.0版本的Linux软件包支持许多Linux发行版，包括较旧的发行版，如CentOS 6.这是conda软件包的另一个好处：尽管被标记为manylinux1兼容（适用于许多版本的linux） ，PyPI上可用的轮子仅支持最少的Ubuntu 16.04，这比许多企业Linux安装要新得多。

    使用NVIDIA GPU可以加速TensorFlow中的许多功能。当运行计算要求严格的深度学习应用程序时，加速度的增加可能特别大。使用pip安装TensorFlow时，必须单独安装GPU支持所需的CUDA和CuDNN库，这增加了入门的负担。当使用conda通过命令“conda install tensorflow-gpu”安装GPU加速版TensorFlow时，这些库会自动安装，其版本已知与tensorflow-gpu软件包兼容。此外，conda将这些库安装到一个位置，在这个位置它们不会干扰可能通过其他方法安装的这些库的其他实例。无论使用pip还是conda安装的tensorflow-gpu，都必须单独安装NVIDIA驱动程序。

    对于许多版本的TensorFlow，conda包可用于多个CUDA版本。例如，CUDA 8.0,9.0和9.2的软件包目前可用于最新版本1.10.0版。 pip包仅支持CUDA 9.0库。在不支持较新版本的CUDA库的系统上工作时，这很重要。最后，因为这些库是通过conda安装的，所以用户可以轻松创建多个环境并比较不同CUDA版本的性能。

    conda TensorFlow软件包还通过使用用于深度神经网络的英特尔®数学核心库（英特尔®MKL-DNN），在CPU上实现更好的性能。从版本1.9.0开始，conda TensorFlow软件包使用英特尔®MKL-DNN库构建，可显着提高性能。例如，图1比较了两个不同图像分类模型的训练和推理的性能，使用使用conda安装的TensorFlow，使用pip安装的相同版本。在许多基准测试中，conda安装版本的性能是pip安装包的速度的八倍多。
    
    <img src="https://raw.githubusercontent.com/littleostar-blog/-conda-install-tensorflow-gpu-on-windows-10/master/images/conda1.png" width="640px" />
    
    图1：使用合成数据在许多常见深度学习模型上训练TensorFlow的性能。 基准测试是在英特尔®至强®黄金6130上进行的。[图片来源](https://www.anaconda.com/blog/developer-blog/tensorflow-in-anaconda/)

    Anaconda为使用优秀的TensorFlow库提供更简单，更快速的体验而感到自豪。 为生产中使用的许多平台添加支持需要花费大量的时间和精力，并确保加速代码仍然稳定且数学上正确。 因此，我们的TensorFlow软件包可能无法与官方TensorFlow轮同时使用。 但是，我们承诺维护我们的TensorFlow软件包，并尽快提供更新。

    有兴趣试用这些TensorFlow套餐吗？ 安装[Anaconda](https://www.anaconda.com/download)或[Miniconda](https://conda.io/miniconda.html)后，创建一个包含TensorFlow的新conda环境并激活它
    
    ```
    conda create -n tensorflow_env tensorflow
    conda activate tensorflow_env
    
    ```
    
    或者是GPU版本
    ```
    conda create -n tensorflow_gpuenv tensorflow-gpu
    conda activate tensorflow_gpuenv
    
    ```

    TensorFlow现已安装并可以使用。对于那些刚接触TensorFlow的人来说，这些[教程](https://www.tensorflow.org/tutorials/)提供了一个入门的好地方。


---

- conda 安装记录

    - python3.6-anaconda-5.2.0-conda-install-tensorflow-gpu-on-windows-10.txt
    ```

    (base) C:\Users\UserXXX>conda create -n tensorflow_gpuenv tensorflow-gpu
    Solving environment: done


    ==> WARNING: A newer version of conda exists. <==
      current version: 4.5.4
      latest version: 4.5.11

    Please update conda by running

        $ conda update -n base conda



    ## Package Plan ##

      environment location: C:\Users\UserXXX\Anaconda3\envs\tensorflow_gpuenv

      added / updated specs:
        - tensorflow-gpu


    The following packages will be downloaded:

        package                    |            build
        ---------------------------|-----------------
        vs2015_runtime-14.15.26706 |       h3a45250_0         2.2 MB
        six-1.11.0                 |           py36_1          21 KB
        keras-applications-1.0.6   |           py36_0          49 KB
        python-3.6.7               |       h33f27b4_0        21.1 MB
        wheel-0.32.2               |           py36_0          52 KB
        cudatoolkit-9.0            |                1       339.8 MB
        libprotobuf-3.6.0          |       h1a1b453_0         2.0 MB
        markdown-3.0.1             |           py36_0         125 KB
        _tflow_select-2.1.0        |              gpu           3 KB
        tensorflow-base-1.11.0     |gpu_py36h6e53903_0       175.1 MB
        vc-14.1                    |       h0510ff6_4           6 KB
        tensorflow-gpu-1.11.0      |       h0d30ee6_0           3 KB
        intel-openmp-2019.0        |              118         1.7 MB
        tensorflow-1.11.0          |gpu_py36h5dc63e2_0           5 KB
        numpy-1.15.3               |   py36ha559c80_0          36 KB
        absl-py-0.5.0              |           py36_0         146 KB
        mkl-2019.0                 |              118       178.1 MB
        mkl_random-1.0.1           |   py36h77b88f5_1         268 KB
        gast-0.2.0                 |           py36_0          15 KB
        grpcio-1.12.1              |   py36h1a1b453_0         1.4 MB
        numpy-base-1.15.3          |   py36h8128ebf_0         3.8 MB
        termcolor-1.1.0            |           py36_1           8 KB
        keras-preprocessing-1.0.5  |           py36_0          52 KB
        h5py-2.8.0                 |   py36h3bdd7fb_2         835 KB
        certifi-2018.10.15         |           py36_0         138 KB
        astor-0.7.1                |           py36_0          44 KB
        tensorboard-1.11.0         |   py36he025d50_0         3.1 MB
        mkl_fft-1.0.6              |   py36hdbbee80_0         120 KB
        setuptools-40.4.3          |           py36_0         576 KB
        cudnn-7.1.4                |        cuda9.0_0       192.3 MB
        protobuf-3.6.0             |   py36he025d50_0         517 KB
        scipy-1.1.0                |   py36h4f6bf74_1        13.6 MB
        ------------------------------------------------------------
                                               Total:       937.1 MB

    The following NEW packages will be INSTALLED:

        _tflow_select:       2.1.0-gpu
        absl-py:             0.5.0-py36_0
        astor:               0.7.1-py36_0
        blas:                1.0-mkl
        certifi:             2018.10.15-py36_0
        cudatoolkit:         9.0-1
        cudnn:               7.1.4-cuda9.0_0
        gast:                0.2.0-py36_0
        grpcio:              1.12.1-py36h1a1b453_0
        h5py:                2.8.0-py36h3bdd7fb_2
        hdf5:                1.10.2-hac2f561_1
        icc_rt:              2017.0.4-h97af966_0
        intel-openmp:        2019.0-118
        keras-applications:  1.0.6-py36_0
        keras-preprocessing: 1.0.5-py36_0
        libprotobuf:         3.6.0-h1a1b453_0
        markdown:            3.0.1-py36_0
        mkl:                 2019.0-118
        mkl_fft:             1.0.6-py36hdbbee80_0
        mkl_random:          1.0.1-py36h77b88f5_1
        numpy:               1.15.3-py36ha559c80_0
        numpy-base:          1.15.3-py36h8128ebf_0
        pip:                 10.0.1-py36_0
        protobuf:            3.6.0-py36he025d50_0
        python:              3.6.7-h33f27b4_0
        scipy:               1.1.0-py36h4f6bf74_1
        setuptools:          40.4.3-py36_0
        six:                 1.11.0-py36_1
        tensorboard:         1.11.0-py36he025d50_0
        tensorflow:          1.11.0-gpu_py36h5dc63e2_0
        tensorflow-base:     1.11.0-gpu_py36h6e53903_0
        tensorflow-gpu:      1.11.0-h0d30ee6_0
        termcolor:           1.1.0-py36_1
        vc:                  14.1-h0510ff6_4
        vs2015_runtime:      14.15.26706-h3a45250_0
        werkzeug:            0.14.1-py36_0
        wheel:               0.32.2-py36_0
        wincertstore:        0.2-py36h7fe50ca_0
        zlib:                1.2.11-h8395fce_2

    Proceed ([y]/n)?

    ```


---

end
