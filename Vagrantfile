
Vagrant.configure("2") do |config|
  config.vm.define :brfe01 do |brfe01|
    brfe01.vm.box = "centos/7"
    brfe01.vm.hostname = "br-fe-01"
    brfe01.vm.network "private_network", ip: "192.168.221.101"
    brfe01.vm.network "public_network", bridge: "wlan0" ,ip: "192.168.0.101"
    brfe01.vm.provision "shell", inline: <<-SHELL

        echo  "ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQDNLW492ZSKmXJh2ugJDsts/mw/NVJdFiWD/sdRxVOlNQi0P1JN9ptg0BIfBrNBUjdRSEY8FPQM54XpnhxF8LBIlB1He5BAr3m5d0NIJv/2fTdwlYpuC+/se92BLdaISIwff9TvNyTRAIaL6zJ1yMK63MPF0jupNwebolwxHnr03ngfaD51eXLruXAwvSb8iBBbsgd37EgIZn1Byd3AQMl8cC21yx1Sf2gbesdrX0VJtEKmZaPksCMix0vbYOyF/dhoPG47NKFW9Y2POqj0f7FcUYc2ucll1B4i3VqhkhyA/DfguvxHoqZcWVRyjgdSu9YZlPwVf9eX0IW+Z7S/xoIh mc@debianmc" >> /home/vagrant/.ssh/authorized_keys

        sudo su

        ssh-keygen -t rsa -N "ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQDNLW492ZSKmXJh2ugJDsts/mw/NVJdFiWD/sdRxVOlNQi0P1JN9ptg0BIfBrNBUjdRSEY8FPQM54XpnhxF8LBIlB1He5BAr3m5d0NIJv/2fTdwlYpuC+/se92BLdaISIwff9TvNyTRAIaL6zJ1yMK63MPF0jupNwebolwxHnr03ngfaD51eXLruXAwvSb8iBBbsgd37EgIZn1Byd3AQMl8cC21yx1Sf2gbesdrX0VJtEKmZaPksCMix0vbYOyF/dhoPG47NKFW9Y2POqj0f7FcUYc2ucll1B4i3VqhkhyA/DfguvxHoqZcWVRyjgdSu9YZlPwVf9eX0IW+Z7S/xoIh mc@debianmc" -f ~/.ssh/id_rsa

        echo  "ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQDNLW492ZSKmXJh2ugJDsts/mw/NVJdFiWD/sdRxVOlNQi0P1JN9ptg0BIfBrNBUjdRSEY8FPQM54XpnhxF8LBIlB1He5BAr3m5d0NIJv/2fTdwlYpuC+/se92BLdaISIwff9TvNyTRAIaL6zJ1yMK63MPF0jupNwebolwxHnr03ngfaD51eXLruXAwvSb8iBBbsgd37EgIZn1Byd3AQMl8cC21yx1Sf2gbesdrX0VJtEKmZaPksCMix0vbYOyF/dhoPG47NKFW9Y2POqj0f7FcUYc2ucll1B4i3VqhkhyA/DfguvxHoqZcWVRyjgdSu9YZlPwVf9eX0IW+Z7S/xoIh mc@debianmc" >> /root/.ssh/authorized_keys

    SHELL
    brfe01.vm.provider "virtualbox" do |vbox|
      vbox.customize ["modifyvm", :id, "--memory", "512"]
      vbox.customize ["modifyvm", :id, "--nicpromisc3", "allow-all"] # eth2
    end
  end
    config.vm.define :chfe01 do |chfe01|
      chfe01.vm.box = "centos/7"
      chfe01.vm.hostname = "ch-fe-01"
      chfe01.vm.network "private_network", ip: "192.168.221.102"
      chfe01.vm.provision "shell", inline: <<-SHELL

        echo  "ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQDNLW492ZSKmXJh2ugJDsts/mw/NVJdFiWD/sdRxVOlNQi0P1JN9ptg0BIfBrNBUjdRSEY8FPQM54XpnhxF8LBIlB1He5BAr3m5d0NIJv/2fTdwlYpuC+/se92BLdaISIwff9TvNyTRAIaL6zJ1yMK63MPF0jupNwebolwxHnr03ngfaD51eXLruXAwvSb8iBBbsgd37EgIZn1Byd3AQMl8cC21yx1Sf2gbesdrX0VJtEKmZaPksCMix0vbYOyF/dhoPG47NKFW9Y2POqj0f7FcUYc2ucll1B4i3VqhkhyA/DfguvxHoqZcWVRyjgdSu9YZlPwVf9eX0IW+Z7S/xoIh mc@debianmc" >> /home/vagrant/.ssh/authorized_keys

        sudo su

        ssh-keygen -t rsa -N "ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQDNLW492ZSKmXJh2ugJDsts/mw/NVJdFiWD/sdRxVOlNQi0P1JN9ptg0BIfBrNBUjdRSEY8FPQM54XpnhxF8LBIlB1He5BAr3m5d0NIJv/2fTdwlYpuC+/se92BLdaISIwff9TvNyTRAIaL6zJ1yMK63MPF0jupNwebolwxHnr03ngfaD51eXLruXAwvSb8iBBbsgd37EgIZn1Byd3AQMl8cC21yx1Sf2gbesdrX0VJtEKmZaPksCMix0vbYOyF/dhoPG47NKFW9Y2POqj0f7FcUYc2ucll1B4i3VqhkhyA/DfguvxHoqZcWVRyjgdSu9YZlPwVf9eX0IW+Z7S/xoIh mc@debianmc" -f ~/.ssh/id_rsa

        echo  "ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQDNLW492ZSKmXJh2ugJDsts/mw/NVJdFiWD/sdRxVOlNQi0P1JN9ptg0BIfBrNBUjdRSEY8FPQM54XpnhxF8LBIlB1He5BAr3m5d0NIJv/2fTdwlYpuC+/se92BLdaISIwff9TvNyTRAIaL6zJ1yMK63MPF0jupNwebolwxHnr03ngfaD51eXLruXAwvSb8iBBbsgd37EgIZn1Byd3AQMl8cC21yx1Sf2gbesdrX0VJtEKmZaPksCMix0vbYOyF/dhoPG47NKFW9Y2POqj0f7FcUYc2ucll1B4i3VqhkhyA/DfguvxHoqZcWVRyjgdSu9YZlPwVf9eX0IW+Z7S/xoIh mc@debianmc" >> /root/.ssh/authorized_keys

    SHELL
      chfe01.vm.provider "virtualbox" do |vbox|
      vbox.customize ["modifyvm", :id, "--memory", "512"]
    end
  end
    config.vm.define :percona1 do |percona1|
      percona1.vm.box = "centos/7"
      percona1.vm.hostname = "percona1"
      percona1.vm.network "private_network", ip: "192.168.221.103"
      percona1.vm.provision "shell", inline: <<-SHELL

        echo  "ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQDNLW492ZSKmXJh2ugJDsts/mw/NVJdFiWD/sdRxVOlNQi0P1JN9ptg0BIfBrNBUjdRSEY8FPQM54XpnhxF8LBIlB1He5BAr3m5d0NIJv/2fTdwlYpuC+/se92BLdaISIwff9TvNyTRAIaL6zJ1yMK63MPF0jupNwebolwxHnr03ngfaD51eXLruXAwvSb8iBBbsgd37EgIZn1Byd3AQMl8cC21yx1Sf2gbesdrX0VJtEKmZaPksCMix0vbYOyF/dhoPG47NKFW9Y2POqj0f7FcUYc2ucll1B4i3VqhkhyA/DfguvxHoqZcWVRyjgdSu9YZlPwVf9eX0IW+Z7S/xoIh mc@debianmc" >> /home/vagrant/.ssh/authorized_keys

        sudo su

        ssh-keygen -t rsa -N "ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQDNLW492ZSKmXJh2ugJDsts/mw/NVJdFiWD/sdRxVOlNQi0P1JN9ptg0BIfBrNBUjdRSEY8FPQM54XpnhxF8LBIlB1He5BAr3m5d0NIJv/2fTdwlYpuC+/se92BLdaISIwff9TvNyTRAIaL6zJ1yMK63MPF0jupNwebolwxHnr03ngfaD51eXLruXAwvSb8iBBbsgd37EgIZn1Byd3AQMl8cC21yx1Sf2gbesdrX0VJtEKmZaPksCMix0vbYOyF/dhoPG47NKFW9Y2POqj0f7FcUYc2ucll1B4i3VqhkhyA/DfguvxHoqZcWVRyjgdSu9YZlPwVf9eX0IW+Z7S/xoIh mc@debianmc" -f ~/.ssh/id_rsa

        echo  "ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQDNLW492ZSKmXJh2ugJDsts/mw/NVJdFiWD/sdRxVOlNQi0P1JN9ptg0BIfBrNBUjdRSEY8FPQM54XpnhxF8LBIlB1He5BAr3m5d0NIJv/2fTdwlYpuC+/se92BLdaISIwff9TvNyTRAIaL6zJ1yMK63MPF0jupNwebolwxHnr03ngfaD51eXLruXAwvSb8iBBbsgd37EgIZn1Byd3AQMl8cC21yx1Sf2gbesdrX0VJtEKmZaPksCMix0vbYOyF/dhoPG47NKFW9Y2POqj0f7FcUYc2ucll1B4i3VqhkhyA/DfguvxHoqZcWVRyjgdSu9YZlPwVf9eX0IW+Z7S/xoIh mc@debianmc" >> /root/.ssh/authorized_keys

    SHELL
      percona1.vm.provider "virtualbox" do |vbox|
      vbox.customize ["modifyvm", :id, "--memory", "512"]
    end
  end
    config.vm.define :percona2 do |percona2|
      percona2.vm.box = "centos/7"
      percona2.vm.hostname = "percona2"
      percona2.vm.network "private_network", ip: "192.168.221.104"
      percona2.vm.provision "shell", inline: <<-SHELL

        echo  "ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQDNLW492ZSKmXJh2ugJDsts/mw/NVJdFiWD/sdRxVOlNQi0P1JN9ptg0BIfBrNBUjdRSEY8FPQM54XpnhxF8LBIlB1He5BAr3m5d0NIJv/2fTdwlYpuC+/se92BLdaISIwff9TvNyTRAIaL6zJ1yMK63MPF0jupNwebolwxHnr03ngfaD51eXLruXAwvSb8iBBbsgd37EgIZn1Byd3AQMl8cC21yx1Sf2gbesdrX0VJtEKmZaPksCMix0vbYOyF/dhoPG47NKFW9Y2POqj0f7FcUYc2ucll1B4i3VqhkhyA/DfguvxHoqZcWVRyjgdSu9YZlPwVf9eX0IW+Z7S/xoIh mc@debianmc" >> /home/vagrant/.ssh/authorized_keys

        sudo su

        ssh-keygen -t rsa -N "ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQDNLW492ZSKmXJh2ugJDsts/mw/NVJdFiWD/sdRxVOlNQi0P1JN9ptg0BIfBrNBUjdRSEY8FPQM54XpnhxF8LBIlB1He5BAr3m5d0NIJv/2fTdwlYpuC+/se92BLdaISIwff9TvNyTRAIaL6zJ1yMK63MPF0jupNwebolwxHnr03ngfaD51eXLruXAwvSb8iBBbsgd37EgIZn1Byd3AQMl8cC21yx1Sf2gbesdrX0VJtEKmZaPksCMix0vbYOyF/dhoPG47NKFW9Y2POqj0f7FcUYc2ucll1B4i3VqhkhyA/DfguvxHoqZcWVRyjgdSu9YZlPwVf9eX0IW+Z7S/xoIh mc@debianmc" -f ~/.ssh/id_rsa

        echo  "ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQDNLW492ZSKmXJh2ugJDsts/mw/NVJdFiWD/sdRxVOlNQi0P1JN9ptg0BIfBrNBUjdRSEY8FPQM54XpnhxF8LBIlB1He5BAr3m5d0NIJv/2fTdwlYpuC+/se92BLdaISIwff9TvNyTRAIaL6zJ1yMK63MPF0jupNwebolwxHnr03ngfaD51eXLruXAwvSb8iBBbsgd37EgIZn1Byd3AQMl8cC21yx1Sf2gbesdrX0VJtEKmZaPksCMix0vbYOyF/dhoPG47NKFW9Y2POqj0f7FcUYc2ucll1B4i3VqhkhyA/DfguvxHoqZcWVRyjgdSu9YZlPwVf9eX0IW+Z7S/xoIh mc@debianmc" >> /root/.ssh/authorized_keys

    SHELL
      percona2.vm.provider "virtualbox" do |vbox|
      vbox.customize ["modifyvm", :id, "--memory", "512"]
    end
  end
    config.vm.define :percona3 do |percona3|
      percona3.vm.box = "centos/7"
      percona3.vm.hostname = "percona3"
      percona3.vm.network "private_network", ip: "192.168.221.105"
      percona3.vm.provision "shell", inline: <<-SHELL

        echo  "ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQDNLW492ZSKmXJh2ugJDsts/mw/NVJdFiWD/sdRxVOlNQi0P1JN9ptg0BIfBrNBUjdRSEY8FPQM54XpnhxF8LBIlB1He5BAr3m5d0NIJv/2fTdwlYpuC+/se92BLdaISIwff9TvNyTRAIaL6zJ1yMK63MPF0jupNwebolwxHnr03ngfaD51eXLruXAwvSb8iBBbsgd37EgIZn1Byd3AQMl8cC21yx1Sf2gbesdrX0VJtEKmZaPksCMix0vbYOyF/dhoPG47NKFW9Y2POqj0f7FcUYc2ucll1B4i3VqhkhyA/DfguvxHoqZcWVRyjgdSu9YZlPwVf9eX0IW+Z7S/xoIh mc@debianmc" >> /home/vagrant/.ssh/authorized_keys

        sudo su

        ssh-keygen -t rsa -N "ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQDNLW492ZSKmXJh2ugJDsts/mw/NVJdFiWD/sdRxVOlNQi0P1JN9ptg0BIfBrNBUjdRSEY8FPQM54XpnhxF8LBIlB1He5BAr3m5d0NIJv/2fTdwlYpuC+/se92BLdaISIwff9TvNyTRAIaL6zJ1yMK63MPF0jupNwebolwxHnr03ngfaD51eXLruXAwvSb8iBBbsgd37EgIZn1Byd3AQMl8cC21yx1Sf2gbesdrX0VJtEKmZaPksCMix0vbYOyF/dhoPG47NKFW9Y2POqj0f7FcUYc2ucll1B4i3VqhkhyA/DfguvxHoqZcWVRyjgdSu9YZlPwVf9eX0IW+Z7S/xoIh mc@debianmc" -f ~/.ssh/id_rsa

        echo  "ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQDNLW492ZSKmXJh2ugJDsts/mw/NVJdFiWD/sdRxVOlNQi0P1JN9ptg0BIfBrNBUjdRSEY8FPQM54XpnhxF8LBIlB1He5BAr3m5d0NIJv/2fTdwlYpuC+/se92BLdaISIwff9TvNyTRAIaL6zJ1yMK63MPF0jupNwebolwxHnr03ngfaD51eXLruXAwvSb8iBBbsgd37EgIZn1Byd3AQMl8cC21yx1Sf2gbesdrX0VJtEKmZaPksCMix0vbYOyF/dhoPG47NKFW9Y2POqj0f7FcUYc2ucll1B4i3VqhkhyA/DfguvxHoqZcWVRyjgdSu9YZlPwVf9eX0IW+Z7S/xoIh mc@debianmc" >> /root/.ssh/authorized_keys

    SHELL
      percona3.vm.provider "virtualbox" do |vbox|
      vbox.customize ["modifyvm", :id, "--memory", "512"]
    end
  end
end
