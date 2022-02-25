FROM ubuntu:18.04
USER root
RUN apt-get update \
    && apt-get install -y software-properties-common \
    && add-apt-repository ppa:deadsnakes/ppa -y \
    && apt-get update \
    && apt-get install -y python3.8
RUN ["/bin/bash","-c","python3 -V"]
WORKDIR /home/python/

RUN echo  "#!/usr/bin/python3 \n\n\
import os \n\n\
x=os.system('date') \n\n\
print(x)" > /home/python/test.py

#ENTRYPOINT ["python3"]
CMD ["python3","/home/python/test.py"]
#CMD ["--version"]
#CMD /bin/bash
