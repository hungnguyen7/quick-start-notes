# Oh My Zsh Install Guide

## 1. Remove Oh My Zsh (if it already installed)

```bash
rm -rf ~/.oh-my-zsh ~/.p10k.zsh ~/.zshrc
```

- `~/.oh-my-zsh` — Oh My Zsh installation folder  
- `~/.p10k.zsh` — Powerlevel10k config file  
- `~/.zshrc` — Zsh config file (backup if needed)  

---

## 2. Install Oh My Zsh

Using curl:

```bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

Or wget:

```bash
sh -c "$(wget https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh -O -)"
```

---

## 3. Install Powerlevel10k Theme (Optional)

```bash
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
```

Edit your `~/.zshrc`:

```bash
ZSH_THEME="powerlevel10k/powerlevel10k"
```

---

## 4. Install Plugins

```bash
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions

git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
```

Add to your `~/.zshrc`:

```bash
plugins=(git zsh-autosuggestions zsh-syntax-highlighting)
```

---

## 5. Reload Shell

```bash
exec zsh
```

or open a new terminal window.

---
