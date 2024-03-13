how to create ssh-key:
ls ~/.ssh   ->check
ssh-keygen -t ed25519 -C "имяфамилия@phystech.edu"
cat ~/.ssh/id_ed25519.pub   ->get key

add to ssh-agent:
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519

add to github:
выберите пункт Settings, найдите слева пункт SSH and GPG keys, нажмите на кнопку New SSH key.
Откроется окно, в котором можно ввести название в поле Title. В поле Key нужно вставить публичный ключ. Его можно получить при помощи команды на вашем компьютере cat ~/.ssh/id_ed25519.pub. Скопируйте ключ из терминала, и вставьте его, после чего нажмите Add SSH key
ssh -T git@github.com   ->check
