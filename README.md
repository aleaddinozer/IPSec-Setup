# IPSec-Setup
You s.hould do each step for both host.
Computers should be connected to the same network.
I have done IPSec conneciton between two Fedora 23 host.
If you get any error youcan check with following command easily
    $ sudo ipsec --verify
When you done with all steps you can check ESP packages in one host when the other one sending ping packages.

Let is say you have two computer and their hostname left and right. And their IP's

    left=192.168.54.12 and right=192.168.54.81
    
  on your left computer  
  
    $ ping 192.168.54.81
At same time on your right compuer

    $ tcpdump -n -i enp3s0 esp
    
 You should write your network device name rather than enps3s0. And you are going to see encapsulated packages on your right computer because you have created a secure connection with IPSec!
    
