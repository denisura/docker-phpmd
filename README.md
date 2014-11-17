docker-phpmd
============

Run PHP Mess Detector (phpmd) in Docker container


Build
--------------------

Build from `Dockerfile`:

    ``` sh
    sudo docker build -t denisura/phpmd .
    ```

Verify build:

    ``` sh
    sudo docker run --rm -it denisura/phpmd --version
    ```

Usage
--------------------

1. Install the `denisura/phpmd` container (optional - this step is performed by Docker automatically when running the container):

    ``` sh
    $ docker pull denisura/phpmd
    ```

2. Define an bash alias that runs this container whenever `phpmd` is invoked on the command line:

	``` sh
	$ echo "alias phpmd='docker run --rm -it -v \$(pwd):/workspace denisura/phpmd'" >> ~/.bashrc
	$ source ~/.bashrc
	```

3. Run phpmd as always:

	``` sh
	$ phpmd --version
	```