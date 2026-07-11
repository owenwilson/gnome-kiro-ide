# gnome kiro-ide

- In this respository, I'm only showing the installation I set up for a linux operating system with GNOME.

## dependencies

```sh
sudo dnf install -y ImageMagick
```

## install kiro-ide

- please check [the kiro-ide web](https://kiro.dev/)

```sh
tar -xzvf kiro-ide-1.0.116-stable-linux-x64.tar.gz
```

```sh
sudo mkdir -p /opt/kiro
```

```sh
sudo mv Kiro /opt/kiro/kiro-ide
```

- change permissions

```sh
sudo chown root: -R /opt/kiro
```

- create a symbolink link

```sh
sudo ln -s /opt/kiro/kiro-ide/bin/kiro
```

## gnome desktop

- download svg file and convert to ico

```sh
magick -density 256x256 -background transparent file-kiro.svg -define icon:auto-resize -colors 256 kiro-icon.ico
```

- copy file

```sh
sudo mkdir -p /opt/kiro/kiro-ico
sudo cp file-kiro.svg /opt/kiro/kiro-ico
```

- configure gnome desktop file

```sh
cp kiro.desktop /home/usert /.local/share/applications/kiro.desktop
```

## reference

- check [kiro-ide](https://kiro.dev/)
