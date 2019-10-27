in the file you want to use the gym environment :

------------------------------------------------------------

steps to complete the adaptor import 

!git clone "https://github.com/CampeanTudor/GoogleColab.git"

!pip install import_ipynb
!pip install ipynb
import import_ipynb
import ipynb
import sys
sys.path.append('GoogleColab/renderGymToColab')

from GoogleColab.renderGymToColab import GymToColabAdaptor as adaptor

-------------------------------------------------------------

first thing after the import is done: call adaptor.start_display()(very important!!!)

when wanting to use gym.make("env_name") use : adaptor.wrap_env(gym.make("env_name"))





if want to call gym.make("env_name") use env = colabAdaptor.wrap_env(gym.make("env_name")) instead
other than make() methods from gym can be used normally

at the end of the script where ev.render() was used call colabAdaptor.show_video()

in examples folder an exaxmple script to use adaptor will exist