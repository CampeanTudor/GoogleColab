in the file you want to use the gym environment :

must install:
 #remove " > /dev/null 2>&1" to see what is going on under the hood
  !pip install gym pyvirtualdisplay > /dev/null 2>&1
  !apt-get install -y xvfb python-opengl ffmpeg > /dev/null 2>&1

  !apt-get update > /dev/null 2>&1
  !apt-get install cmake > /dev/null 2>&1
  !pip install --upgrade setuptools 2>&1
  !pip install ez_setup > /dev/null 2>&1
  !pip install gym[atari] > /dev/null 2>&1
  !pip install pyglet==1.3.2

---------------------------------------------------------------

must import:
import gym
  from gym import logger as gymlogger
  from gym.wrappers import Monitor
  gymlogger.set_level(40) #error only
  import tensorflow as tf
  import numpy as np
  import random
  import matplotlib
  import matplotlib.pyplot as plt
  %matplotlib inline
  import math
  import glob
  import io
  import base64
  from IPython.display import HTML
  from IPython import display as ipythondisplay
  from pyvirtualdisplay import Display
  display = Display(visible=0, size=(1400, 900))
  display.start()

-------------------------------------------------------------


if want to call gym.make("env_name") use env = colabAdaptor.wrap_env(gym.make("env_name")) instead
other than make() methods from gym can be used normally

at the end of the script where ev.render() was used call colabAdaptor.show_video()