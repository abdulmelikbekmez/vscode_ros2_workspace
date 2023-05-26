FROM osrf/ros:melodic-desktop-full

# nvidia-container-runtime
ENV NVIDIA_VISIBLE_DEVICES \
        ${NVIDIA_VISIBLE_DEVICES:-all}
ENV NVIDIA_DRIVER_CAPABILITIES \
        ${NVIDIA_DRIVER_CAPABILITIES:+$NVIDIA_DRIVER_CAPABILITIES,}graphics

# Create the user
ARG USER
ARG PASS
RUN useradd -m $USER && echo "$USER:$PASS" | chpasswd && adduser $USER sudo

USER $USER

ARG WORKSPACE
