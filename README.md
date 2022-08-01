# Bootcamp
test tasks


## Test 1
There is string s = "Python Bootcamp". Write the code that hashes string.

```python
def hash_string(s = "Python Bootcamp"):
    from hashlib import sha256
    return sha256(s.encode('utf-8')).hexdigest()
    
hash_string()
```

## Test 2
You are working on a project for TikTok. The future project will be a web-site of all public GIF images. You need to write a function that converts TikTok video to GIF. The input parameter is url address of TikTok video, i.e.  ["TikTok example"](https://v16m-webapp.tiktokcdn-us.com/ed129ecb01ab00e202682e99f68a9288/62e7cb0d/video/tos/useast5/tos-useast5-pve-0068-tx/d69985b1677b4a73a584b56d604011ca/?a=1988&ch=0&cr=0&dr=0&lr=tiktok_m&cd=0%7C0%7C1%7C0&cv=1&br=4020&bt=2010&cs=0&ds=3&ft=ebtHKH-qMyq8ZjFl1we2N9befl7Gb&mime_type=video_mp4&qs=0&rc=OTU4MzU0NzVnaDpnOGg8OEBpajM5Z2c6ZmYzZTMzZzczNEAuMC9jLWBgNmExMzJfY18tYSMxX28vcjRnMGRgLS1kMS9zcw%3D%3D&l=20220801064449EF653E99EF32BC2EAB55). The output parameter is path to GIF image, i.e. "/home/user/TikTok-example-1.gif".

```python
def tiktok_gif(url):
    
    from moviepy.editor import VideoFileClip
    from os.path import abspath
    
    name = input("Enter the name for the video\n")
    
    urllib.request.urlretrieve(url,name + '.mp4') 
    clip = VideoFileClip(name + '.mp4')
    
    
    gif_name="TikTok_" + name + ".gif"
    clip.write_gif("output.gif")
    
    return abspath(gif_name)
    
link ="https://v16m-webapp.tiktokcdn-us.com/ed129ecb01ab00e202682e99f68a9288/62e7cb0d/video/tos/useast5/tos-useast5-pve-0068-tx/d69985b1677b4a73a584b56d604011ca/?a=1988&ch=0&cr=0&dr=0&lr=tiktok_m&cd=0%7C0%7C1%7C0&cv=1&br=4020&bt=2010&cs=0&ds=3&ft=ebtHKH-qMyq8ZjFl1we2N9befl7Gb&mime_type=video_mp4&qs=0&rc=OTU4MzU0NzVnaDpnOGg8OEBpajM5Z2c6ZmYzZTMzZzczNEAuMC9jLWBgNmExMzJfY18tYSMxX28vcjRnMGRgLS1kMS9zcw%3D%3D&l=20220801064449EF653E99EF32BC2EAB55"
tiktok_gif(link)
```
