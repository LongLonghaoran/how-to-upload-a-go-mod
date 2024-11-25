如何将自己的go mod项目推送到公共仓库以让他人可通过go get下载

1.创建自己的go mod项目
go mod init how-to-upload-a-go-mod
2.给该项目搭上一个版本标签
git tag v0.0.1
3.推送到github.com上面，加上--tags把标签也推送上去
git push -u origin --tags main
4.在其他机器上明确指定版本号来拉取该mod
go get -u github.com/LongLonghaoran/how-to-upload-a-go-mod@v0.0.1
