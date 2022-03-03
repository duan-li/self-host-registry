

https://gabrieltanner.org/blog/docker-registry

# add user and password

```bash

cans run adduser htpasswd -Bc filename username

```





```
    1  ls
    2  apt-get remove docker docker-engine docker.io containerd runc
    3  apt update
    4  apt-get install     ca-certificates     curl     gnupg     lsb-release -y
    5  curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
    6  echo   "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu \
  $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
    7  apt update
    8  apt-get install docker-ce docker-ce-cli containerd.io -y
    9  docker
   10  docker images
   11  df -h
   12  apt-cache madison docker-ce
   13  docker run hello-world
   14  ls
   15  docker-compose
   16  apt install docker-compose
   17  ls
   18  mkdir hub
   19  cd hub
   20  git
   21  git init
   22  ls
   23  nano docker-compose.yaml
   24  cd ..
   25  git clone git@github.com:duan-li/cans.git
   26  ls
   27  git clone https://github.com/duan-li/cans.git
   28  ls
   29  cd cans
   30  ls
   31  cd scripts/
   32  ls
   33  ./cans
   34  cp cans /bin/
   35  cans
   36  cd
   37  ls
   38  cd hub
   39  ls
   40  cans init
   41  ca docker-compose.y
   42  ls
   43  ls -lh
   44  cat docker-compose.yml
   45  rm docker-compose.yml
   46  nano cans.conf
   47  ls
   48  cat docker-compose.yaml
   49  mkdir auth
   50  nano docker-compose.yaml
   51  cans run adduser testuser testpass > /auth/htpasswd
   52  cans run adduser
   53  nano docker-compose.yaml
   54  cans run adduser
   55  nano docker-compose.yaml
   56*
   57  cans run adduser testuser testpass > /auth/htpasswd
   58  docker-compose run adduser testuser testpass > /auth/htpasswd
   59  docker-compose run adduser testuser testpass > auth/htpasswd
   60  ls
   61  cd auth
   62  ls
   63  cat htpasswd
   64  ls -lh
   65  ls
   66  cd ..
   67  cans up
   68  docker ps -a
   69  ls
   70  docker images
   71  docker tag hello-world localhost:5000/hw
   72  docker push localhost:5000/hw
   73  docker images
   74  cd /var
   75  ls
   76  cd images
   77  ls
   78  cd ..
   79  ls
   80  docker ps
   81  docker logs registry
   82  cd
   83  ls
   84  cd hub
   85  ls
   86  cans down
   87  nano docker-compose.yaml
   88  cans up
   89  docker push localhost:5000/hw
   90  docker login localhost:5000
   91  history
   92  cat docker-compose.yaml
   93  history
   94  cans run adduser test test > auth/htpasswd
   95  ls auth
   96  ls auth -ls
   97  ls
   98  cans down
   99  cans up
  100  history
  101  docker login localhost:5000
  102  docker logs registry
  103  cans down
  104  nano docker-compose.yaml
  105  cans show
  106  cans up
  107  docker login localhost:5000
  108  ls
  109  cd auth
  110  ls
  111  cat htpasswd
  112  ls
  113  rm htpasswd
  114  ls
  115  cd ..
  116  ls
  117  nano docker-compose.yaml
  118  history
  119  cans run adduser test test > auth/htpasswd
  120  ls
  121  cd auth
  122  ls
  123  cat htpasswd
  124  ls
  125  docker run   --entrypoint htpasswd   httpd:2 -Bc htpasswd testuser
  126  docker run   --entrypoint htpasswd   httpd:2 -Bc htpasswd test test
  127  docker run   --entrypoint htpasswd   httpd:2 -B htpasswd test test
  128  ls
  129  cat htpasswd
  130  docker run -it   --entrypoint htpasswd   httpd:2 -B htpasswd test test
  131  docker run -it   --entrypoint htpasswd   httpd:2 -Bc htpasswd test test
  132  docker run -it   --entrypoint htpasswd   httpd:2 -Bn htpasswd test test
  133  docker run -it   --entrypoint htpasswd   httpd:2 -nb htpasswd test test
  134  docker run -it   --entrypoint htpasswd   httpd:2 -nb test test
  135  docker run -it   --entrypoint htpasswd   httpd:2 -nb test test > ht
  136  ls
  137  rm ht
  138  docker run -it   --entrypoint htpasswd   httpd:2 -nb test test > htpasswd
  139  cat htpasswd
  140  cd ..
  141  cans show
  142  cans down
  143  cans up
  144  history
  145  docker login localhost:5000
  146  docker ps -a
  147  cd auth/
  148  ls
  149  cat htpasswd
  150  docker rm $(docker ps -aq)
  151  docker ps -a
  152  ls
  153  cd ..
  154  ls
  155  nano docker-compose.yaml
  156  docker logs regisry
  157  docker logs registry
  158  ls
  159  nano docker-compose.yaml
  160  cans down
  161  cans up
  162  history
  163  docker push localhost:5000/hw
  164  docker rmi localhost:5000/hw
  165  docker images
  166  docker pull localhost:5000/hw
  167  docker rmi localhost:5000/hw
  168  docker run localhost:5000/hw
  169  cd /var/images
  170  ls
  171  cd docker
  172  ls
  173  cd registry/
  174  ls
  175  cd v2/
  176  ls
  177  cd repositories/
  178  ls
  179  docker images
  180  docker tag httpd:2 206.189.82.224:5000/httpd:2
  181  docker push 206.189.82.224:5000/httpd:2
  182  ls
  183  cd
  184  ls
  185  cd hub
  186  ls
  187  cat docker-compose.yaml
  188  ls
  189  apt install apache2-utils -y
  190  ls
  191  cd auth
  192  htpasswd -Bc registry.password testuser
  193  ls
  194  cat registry.password
  195  cat htpasswd
  196  ls
  197  cd ..
  198  ls
  199  nano docker-compose.yaml
  200  cans down
  201  cans up
  202  docker login localhost:5000
  203  ls
  204  nano docker-compose.yaml
  205  ls
  206  cans run adduser user test
  207  cans run adduser user.dd test
  208  cans run adduser test
  209  nano docker-compose.yaml
  210  cans run adduser test
  211  cans run adduser test tt
  212  cd auth
  213  ls
  214  cd ..
  215  ls
  216  nano docker-compose.yaml
  217  cans run adduser test tt
  218  ls
  219  cd auth
  220  ls
  221  cd ..
  222  ls
  223  nano docker-compose.yaml
  224  cans run adduser file tt
  225  cans run adduser htpasswd -Bc file tt
  226  cd auth
  227  ls
  228  cat file
  229  cd ..
  230  ls
  231  nano README.md
  232  git init
  233  ls
  234  nano .git/config
  235  ls
  236  history

```
