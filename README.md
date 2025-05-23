# spark-tts

```
Install xcode-select and command line tools for XCode
```

```
% /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

```
% cat .zshrc                                           
set -o vi

# Set path for brew
export PATH=$PATH:/opt/homebrew/bin

# Load pyenv automatically by appending
# the following to 
# ~/.bash_profile if it exists, otherwise ~/.profile (for login shells)
# and ~/.bashrc (for interactive shells) :

export PYENV_ROOT="$HOME/.pyenv"
[[ -d $PYENV_ROOT/bin ]] && export PATH="$PYENV_ROOT/bin:$PATH"
eval "$(pyenv init - bash)"

# Restart your shell for the changes to take effect.
# Load pyenv-virtualenv automatically by adding
# the following to ~/.bashrc:
eval "$(pyenv virtualenv-init -)"
```

```
source .zshrc
```

```
% brew install xz
% brew install git-lfs
```

```
% pyenv install 3.12
% pyenv virtualenv 3.12 venv_spark_tts
% pyenv activate venv_spark_tts

```

```
% pip install -r requirements.txt
```

```
% mkdir -p /Users/statisticalfx/Development
% cd /Users/statisticalfx/Development
% git clone https://github.com/SparkAudio/Spark-TTS.git
% cd Spark-TTS
% git clone https://huggingface.co/SparkAudio/Spark-TTS-0.5B pretrained_models/Spark-TTS-0.5B
```

```
 % huggingface-cli login

    _|    _|  _|    _|    _|_|_|    _|_|_|  _|_|_|  _|      _|    _|_|_|      _|_|_|_|    _|_|      _|_|_|  _|_|_|_|
    _|    _|  _|    _|  _|        _|          _|    _|_|    _|  _|            _|        _|    _|  _|        _|
    _|_|_|_|  _|    _|  _|  _|_|  _|  _|_|    _|    _|  _|  _|  _|  _|_|      _|_|_|    _|_|_|_|  _|        _|_|_|
    _|    _|  _|    _|  _|    _|  _|    _|    _|    _|    _|_|  _|    _|      _|        _|    _|  _|        _|
    _|    _|    _|_|      _|_|_|    _|_|_|  _|_|_|  _|      _|    _|_|_|      _|        _|    _|    _|_|_|  _|_|_|_|

    To login, `huggingface_hub` requires a token generated from https://huggingface.co/settings/tokens .
```

```
% export PYTORCH_ENABLE_MPS_FALLBACK=1
% pwd         
/Users/statisticalfx/Development/Spark-TTS

% python webui.py --device 0
```

