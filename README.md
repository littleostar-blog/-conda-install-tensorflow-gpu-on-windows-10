###  conda install tensorflow-gpu

---

- Reference：
  - [https://www.anaconda.com/blog/developer-blog/tensorflow-in-anaconda/](https://www.anaconda.com/blog/developer-blog/tensorflow-in-anaconda/)
  - [https://towardsdatascience.com/stop-installing-tensorflow-using-pip-for-performance-sake-5854f9d9eb0c](https://towardsdatascience.com/stop-installing-tensorflow-using-pip-for-performance-sake-5854f9d9eb0c)

---

#### how to install tensorflow_gpu use conda
    
    ```
    conda create -n tensorflow_env tensorflow
    conda activate tensorflow_env
    
    ```
    
    
    ```
    conda create -n tensorflow_gpuenv tensorflow-gpu
    conda activate tensorflow_gpuenv
    
    ```


---

- conda install log

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
