Vagrant.configure("2") do |config|
  # Веб-сервер
  config.vm.define "web" do |web|
    web.vm.box = "ubuntu/focal64"
    web.vm.network "forwarded_port", guest: 80, host: 8080
    web.vm.hostname = "web"
    web.vm.network "private_network", type: "static", ip: "192.168.56.2" # Призначаємо фіксовану IP-адресу
  end

  # Сервер бази даних
  config.vm.define "db" do |db|
    db.vm.box = "ubuntu/focal64"
    db.vm.network "forwarded_port", guest: 3306, host: 3306
    db.vm.hostname = "db"
    db.vm.network "private_network", type: "static", ip: "192.168.56.3" # Призначаємо фіксовану IP-адресу
  end
end
