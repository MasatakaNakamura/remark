You can easily build your own version of remark in the following steps:

```sh
git clone https://github.com/gnab/remark.git
cd remark
git submodule update --init --recursive
npm install
node make
```