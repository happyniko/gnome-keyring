
# ------------------------------------------------------------------------------
# The ssh-agent component code

noinst_LTLIBRARIES += \
	libgkd-ssh-agent.la

libgkd_ssh_agent_la_SOURCES = \
	daemon/ssh-agent/gkd-ssh-agent.c \
	daemon/ssh-agent/gkd-ssh-agent.h \
	daemon/ssh-agent/gkd-ssh-agent-private.h \
	daemon/ssh-agent/gkd-ssh-agent-ops.c \
	daemon/ssh-agent/gkd-ssh-agent-proto.c
libgkd_ssh_agent_la_CFLAGS = \
	$(DAEMON_CFLAGS)

# ------------------------------------------------------------------------------
# Standalone binary

noinst_PROGRAMS += \
	gkd-ssh-agent-standalone

gkd_ssh_agent_standalone_SOURCES = \
	daemon/ssh-agent/gkd-ssh-agent-standalone.c
gkd_ssh_agent_standalone_CFLAGS = \
	$(DAEMON_CFLAGS)
gkd_ssh_agent_standalone_LDADD = \
	libgkd-ssh-agent.la \
	libegg-buffer.la \
	libegg-secure.la \
	$(DAEMON_LIBS)
