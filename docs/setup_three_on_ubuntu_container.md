1. $ apt-get install  build-essential libxi-dev libglu1-mesa-dev libglew-dev pkg-config mesa-utils  xvfb libgl1-mesa-dri libglapi-mesa libosmesa6 npm curl wget

2. $ export DISPLAY=:1           

3. $ Xvfb :1 -screen 0 1920x1080x24 &

4. $ npm install -g n

5. $ n stable

6. $ PATH="$PATH"

ili treba restartat bash 

7. node server.js