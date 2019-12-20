# opencv4.1.2_Catalina10.15.2

## 1.Homebrew install

아래 명령어를 이용하여 Homebrew를 받습니다.
~~~
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
~~~


homebrew 를 이용해 프로그램을 설치 전 매번 update를 해주는 것이 좋습니다.
~~~
brew update
~~~

opencv를 설치 하였으면 Xcode에 이식하기 위해 플래그를 확인해야 합니다.
~~~
brew install opencv
~~~

---

pkg-config install & Linker Flag 추출
*Linker Flag 는 xcode에게 라이브러리를 참조하라고 하는 것입니다.
~~~
brew install pkg-config
~~~

설치 했으니 이제 Lingker Flag를 알아내봅니다.
~~~
pkg-config --cflags --libs opencv4
~~~

Xcode
> Header Search Paths 에
~~~
/usr/local/include
~~~
> Library Search Paths 에
~~~
/usr/local/lib
~~~
