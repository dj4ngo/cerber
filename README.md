# Bouncer
A straightforward tool for generate seccomp json

## Usage
```sh
$ python bouncer # display output on stdout
{
    "defaultAction": "SCMP_ACT_ERRNO", 
    "architecture": [
        "SCMP_ARCH_X86_64", 
        "SCMP_ARCH_X86", 
        "SCMP_ARCH_X32"
    ], 
    "syscalls": [
        {
            "action": "SCMP_ACT_ALLOW", 
            "args": [], 
            "name": "read"
        }, 
        ...
        {
            "action": "SCMP_ACT_ALLOW", 
            "args": [], 
            "name": "execve"
        }, 
        {
            "action": "SCMP_ACT_ALLOW", 
            "args": [], 
            "name": "arch_prctl"
        }
    ]
}
```

Or save output to json file
```sh
$ python bouncer > seccomp.json # save output inside seccomp.json file
```
