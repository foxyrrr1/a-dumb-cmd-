sudo add-apt-repository ppa:lamarque/lact -y && \
sudo apt update && \
sudo apt install lact maliit-keyboard qt6-virtualkeyboard-layers steamdeck-firmware amdgpu-install -y && \
sudo systemctl enable --now lactd && \
sudo udevadm control --reload-rules && sudo udevadm trigger && \
gsettings set org.gnome.desktop.a11y.applications screen-keyboard-enabled true
