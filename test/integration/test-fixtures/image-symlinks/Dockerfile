FROM busybox:1.36@sha256:023917ec6a886d0e8e15f28fb543515a5fcd8d938edb091e8147db4efed388ee
# link with previous data
ADD file-1.txt .
RUN ln -s ./file-1.txt link-1
# link with future data
RUN ln -s ./file-2.txt link-2
ADD file-2.txt .
# link with current data
RUN echo "file 3" > file-3.txt && ln -s ./file-3.txt link-within
# multiple links (link-indirect > link-2 > file-2.txt)
RUN ln -s ./link-2 link-indirect
# override contents / resolution
ADD new-file-2.txt file-2.txt
# dead link (link-indirect > [non-existant file])
RUN unlink link-2
