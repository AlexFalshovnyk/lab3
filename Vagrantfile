
Vagrant.configure("2") do |config|
  config.vm.box = "matthiasmullie/debian9-arm64"
  config.vm.box_version = "1.0.0"
  
  config.vm.provision "shell", inline: <<-SHELL
    
     find / -type l
     find / -type b -or -type c | wc -l
     find / -type d -perm -1000
     ln -s /etc/hostname /tmp/softlink
     sudo adduser valera_user
     touch /home/valera_user/testuser_data
     sudo chown valera_user:valera_user /home/valera_user/testuser_data
   SHELL
end
