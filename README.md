sudo add-apt-repository ppa:lamarque/lact -y && \
sudo nala update && \
sudo nala install lact maliit-keyboard qtvirtualkeyboard-plugin qt6-virtualkeyboard-layers git curl -y && \
sudo systemctl enable --now lactd && \
sudo udevadm control --reload-rules && sudo udevadm trigger && \
kwriteconfig6 --file kwinrc --group Wayland --key VirtualKeyboardEnabled true && \
qdbus6 org.kde.KWin /KWin reconfigure
