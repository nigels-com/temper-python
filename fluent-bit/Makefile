.PHONY: install start stop status logs

NAME   ?= temper-python
PREFIX ?= /usr/local

install:
	NAME=${NAME} PREFIX=$(PREFIX) envsubst < temper-python.fluent-bit | tee ${PREFIX}/etc/fluent-bit/temper-python.cfg
	NAME=${NAME} PREFIX=$(PREFIX) envsubst < temper-python.systemd | tee /etc/systemd/system/$(NAME).service
	sudo systemctl daemon-reload

start:
	systemctl start $(NAME)

stop:
	systemctl stop $(NAME)

status:
	systemctl status $(NAME) || true

logs:
	journalctl -f -u $(NAME)
