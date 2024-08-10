# Install Zsh + powerlevel10k and autosugestion on Linux
1. Install Zsh
```bash
sudo apt install zsh
```
Link: https://github.com/ohmyzsh/ohmyzsh/wiki/Installing-ZSH

2. Verify zsh version
```bash
zsh --version
```

3. Establish zsh by default:
```bash
chsh -s $(which zsh)
```

4. Install Ohmyzhs
```bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

```
Link: https://github.com/ohmyzsh/ohmyzsh?tab=readme-ov-file

5. Install MesloLGS fonts

Link: https://github.com/romkatv/powerlevel10k?tab=readme-ov-file#meslo-nerd-font-patched-for-powerlevel10k

6. Clone repository:
```bash
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
```

7. Edit your file 
**Vim**
```bash
vi ~/.zshrc
```

**Vim**
```bash
nano ~/.zshrc
```

6.1. Replace the theme between quotes:
```bash
ZSH_THEME="powerlevel10k/powerlevel10k
```

## Plugins
7. Clone zsh-syntax-highlighting 

```bash
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
```

8. Clone zsh-autosuggestions
```bash
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
```

9. Edit your file and search `plugins`

**Vim**
```bash
vi ~/.zshrc
```
**Edit**
```bash
plugins=( git zsh-syntax-highlighting zsh-autosuggestions )
```

10. Finally refresh your bash:

```bash
source ~/.zshrc
```