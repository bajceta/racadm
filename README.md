# Dell racadm on Centos


# Examples
## Get system info
   `docker run bajceta/racadm -r 10.12.10.62 -u root -p root getsysinfo`

## Upload iDRAC ssl key
   `docker run -v ${PWD}:/out -it bajceta/racadm -r 10.12.10.61 -u root -p root sslkeyupload -t 1 -f /out/i-r620-1-key.pem`

   `docker run -v ${PWD}:/out -it bajceta/racadm -r 10.12.10.61 -u root -p root sslcertupload -t 1 -f /out/i-r620-1.pem`


## Enable vnc
   `docker run -it bajceta/racadm -r 10.12.10.61 -u root -p root set idrac.vncserver.enable Enabled`

   `docker run -it bajceta/racadm -r 10.12.10.61 -u root -p root set idrac.vncserver.Password reallyStrongPassword`

