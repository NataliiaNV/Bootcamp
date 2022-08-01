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
You are working on a project for TikTok. The future project will be a web-site of all public GIF images. You need to write a function that converts TikTok video to GIF. The input parameter is url address of TikTok video, i.e. "TikTok example". The output parameter is path to GIF image, i.e. "/home/user/TikTok-example-1.gif".

