# CustomCamera([中文说明](https://github.com/jinguangyue/CustomCamera/blob/master/README_CN.md))
It's a custom Camera Project. Now it includes Basic camera functions. Then I Will fill many functions. E.g Front and rear mirror switch， Flash Mode， Delay shooting， Square viewfinder，Then i will Add watermark effect and Camera2 Api.

You can download the apk file folder , and then install the apk demo

**If you want to define your own interface , then you can view the detailed CameraActivity and change its layout file activity_camera.xml.**


**Some notes**

In My MainActivity Such calls:

```
CameraUtil.getInstance().camera(MainActivity.this);
```

Then onActivityResult get the picture returned , you can also create your Activity calls like this.
```
@Override
protected void onActivityResult(int requestCode, int resultCode, Intent data) {
    super.onActivityResult(requestCode, resultCode, data);

    if(resultCode != AppConstant.RESULT_CODE.RESULT_OK){
        return;
    }

    if(requestCode == AppConstant.REQUEST_CODE.CAMERA){
        String img_path = data.getStringExtra(AppConstant.KEY.IMG_PATH);
        img.setImageURI(Uri.parse(img_path));
    }
}
```
