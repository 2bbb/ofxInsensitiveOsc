# ofxInsensitiveOsc

this ofxOscReceiver doesn't terminate when receive broken packet.

based on `ofxOsc@oF0.9.2`.

this addon trashes broken packets with error messages.

i think, this error handling is not best but, as better than app terminate.

(maybe i will post PR or issue about this problem to openFrameworks community.)

## Notice

**PLEASE USE AT YOUR OWN RISK.**

## How to use

basicly, same as `ofxOsc`.

add 1 future.
got event as:

```
void setup() {
    receiver.setup(8888);
    ofAddListener(receiver.gotOscError, this, &ofApp::oscError);
}

void oscError(std::string &what) {
    ofLogWarning() << what;
}
```

## Update History

### 2016/03/16 ver 0.02 release

* simplify.
* add future: notify gotError event with error message.
* post PR on [openFrameworks#4998](https://github.com/openframeworks/openFrameworks/pull/4998) without notify event. (maybe if occurs diff of API, will not merge while oF0.9.x) and, i can't get no.5000.

### 2016/02/26 ver 0.01 release

* first aid.

## License

MIT License.

## Author

* Ross Bencina 
* rossb@audiomulch.com
* Copyright (c) 2004

## Modify by

* ISHII 2bit [bufferRenaiss co., ltd.]
* ishii[at]buffer-renaiss.com

## Special thanks

* [TOMOTO Yusuke](https://github.com/yusuketomoto)
* [HANAI Yuya](https://github.com/hanasaan)


