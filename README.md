# docker-vncrecorder
Run VNC recorder in order to record VNC stream to flv.

## Built with
- latest debian
- python-pip
- vnc2flv 20100207

## Start recording$

    docker run -d --name vncrecorder -v ${VNC_DIR}:/vnc softsam/vncrecorder -o /vnc/record.flv VNC_HOSTNAME_OR_IP
    
## Stop recording

    docker kill -s INT vncrecorder
