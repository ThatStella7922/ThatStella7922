## Notice
This text file is meant to accompany the video on my YouTube channel: [How to install Windows 11 on any x64 UEFI-capable PC](https://youtu.be/wZzmqYX6fmw)


### Commands used in the video
[At 4:50] Set the ID of the recovery partition:\
`set id="de94bba4-06d1-4d40-a16a-bfd50179d6ac"`

[At 5:03] Set the attribute of the recovery partition:\
`gpt attributes=0x8000000000000001`

[At 5:39] Deploy Windows to drive C: using:\
`dism /apply-image /imagefile:d:\sources\install.wim /index:1 /applydir:C:`
