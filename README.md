###  conda install tensorflow-gpu

---

- 翻译来源：
  - [https://www.anaconda.com/blog/developer-blog/tensorflow-in-anaconda/](https://www.anaconda.com/blog/developer-blog/tensorflow-in-anaconda/)
  - https://towardsdatascience.com/stop-installing-tensorflow-using-pip-for-performance-sake-5854f9d9eb0c


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
    
    <img src="" width="640px" />
    
    图1：使用合成数据在许多常见深度学习模型上训练TensorFlow的性能。 基准测试是在英特尔®至强®黄金6130上进行的。(图片来源:  https://www.anaconda.com/blog/developer-blog/tensorflow-in-anaconda/)

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

end
