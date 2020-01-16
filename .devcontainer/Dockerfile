FROM mirisbowring/texlive_ctan_full:2019

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update -qq && apt-get install -y \
  locales \
  curl \
  perlbrew \
  && rm -rf /var/lib/apt/lists/*

# https://medium.com/@kombustor/vs-code-docker-latex-setup-f84128c6f790
# generating locales
RUN sed -i -e 's/# en_US.UTF-8 UTF-8/en_US.UTF-8 UTF-8/' /etc/locale.gen && \
  dpkg-reconfigure --frontend=noninteractive locales && \
  update-locale LANG=en_US.UTF-8
ENV LANGUAGE=en_US.UTF-8 LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8


RUN curl -L http://cpanmin.us | perl - App::cpanminus && \
  cpanm YAML::Tiny File::HomeDir Unicode::GCString Log::Log4perl Log::Dispatch Log::Dispatch::File

# https://github.com/docker-library/golang/issues/148#issuecomment-355082955
RUN mkdir -p /root/.ssh/ && ssh-keyscan github.com >> /root/.ssh/known_hosts
