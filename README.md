# python_ml

Going through Aurélien Géron's [Hands-On Machine Learning with Scikit-Learn & TensorFlow](http://shop.oreilly.com/product/0636920052289.do)

Chapter 2 is where it really becomes a workbook, but Chapter 1 is definitely worth the read.

## How I set up my environment

The book gives you some options, but I went with making a project-specific virtual environment, because I work on a lot of other python stuff, too.

- Create the venv
  - I'm using python 3.6, so have that installed. I think venv comes with it, but you might have to install it with pip3
  - cd to your project directory, mine is called python_ml and lives on my Desktop. Type the following into your terminal (or Powershell if you're a Windows person, but I haven't tested this in Windows so you might need extra help.)
    - `cd ~/Desktop/python_ml`
  - `python3 -m venv ./env`
    - this will create a directory in your project folder called "env" and store your virtual environment files there
  - `echo "env/" >> .gitignore`
    - This will let git ignore the virtual environment files, which makes the project more portable between systems (I use Ubuntu Linux and Mac OS) _BUT_ it will also make these terminal steps necessary to perform on every system you're using.
  - Activate the virtual environment
    - `source ./env/bin/activate`
    - Your terminal cursor should now be prepended with (env) indicating that you are now in the virtual environment.
    - To exit at any time, type `deactivate` and press Enter or Return or whatever it's called on your keyboard.
    - While you are in the virtual environment, python packages you install with pip will not be globally installed to your system, preventing interference with other projects.
  - Install the project requirements:
    - `pip3 install --upgrade jupyter matplotlib numpy pandas scipy scikit-learn`
    - pip3 is the Python package manager, this line tells it to install that list of packages, and to --upgrade any in that list if they are already installed.
  - Test that the installation worked:
    - `python3 -c "import jupyter, matplotlib, numpy, pandas, scipy, sklearn"`
    - If you can run that line in your terminal without getting any errors, then good!
  - Activate a Jupyter server:
    - `jupyter notebook`
    - This should open localhost:8888/tree in your browser. If so, continue following along in the book if you've got it.

That's it, you're ready to GO! The real fun starts on page 42 of the edition I'm reading with is the March 2017 First Edition.
