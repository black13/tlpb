set(Main_SRCS
 i6d_ucase_cl.c
i6d_ucase_sv.c
id_echo_cl.c
id_echo_sv.c
inet_sockets.c
is_echo_cl.c
is_echo_inetd_sv.c
is_echo_sv.c
is_echo_v2_sv.c
is_seqnum_cl.c
is_seqnum_sv.c
is_seqnum_v2_cl.c
is_seqnum_v2_sv.c
list_host_addresses.c
scm_cred_recv.c
scm_cred_send.c
scm_rights_recv.c
scm_rights_send.c
socknames.c
t_gethostbyname.c
t_getservbyname.c
ud_ucase_cl.c
ud_ucase_sv.c
unix_sockets.c
us_abstract_bind.c
us_xfr_cl.c
us_xfr_sv.c
us_xfr_v2_cl.c
us_xfr_v2_sv.c
)
include_directories(${PROJECT_SOURCE_DIR}/daemons)

find_package( Threads )


ADD_EXECUTABLE( i6d_ucase_cl i6d_ucase_cl.c unix_sockets.c )
target_link_libraries( i6d_ucase_cl lib )
ADD_EXECUTABLE( i6d_ucase_sv i6d_ucase_sv.c unix_sockets.c)
target_link_libraries( i6d_ucase_sv lib )
ADD_EXECUTABLE( id_echo_cl id_echo_cl.c unix_sockets.c inet_sockets.c)
target_link_libraries( id_echo_cl lib )

ADD_EXECUTABLE( is_echo_cl is_echo_cl.c unix_sockets.c inet_sockets.c)
target_link_libraries( is_echo_cl lib )
ADD_EXECUTABLE( is_echo_inetd_sv is_echo_inetd_sv.c unix_sockets.c)
target_link_libraries( is_echo_inetd_sv lib )
ADD_EXECUTABLE( is_echo_v2_sv is_echo_v2_sv.c inet_sockets.c unix_sockets.c ${PROJECT_SOURCE_DIR}/daemons/become_daemon.c)
target_link_libraries( is_echo_v2_sv lib )
ADD_EXECUTABLE( is_seqnum_cl is_seqnum_cl.c unix_sockets.c read_line.c)
target_link_libraries( is_seqnum_cl lib )
ADD_EXECUTABLE( is_seqnum_sv is_seqnum_sv.c unix_sockets.c read_line.c)
target_link_libraries( is_seqnum_sv lib )
ADD_EXECUTABLE( is_seqnum_v2_cl is_seqnum_v2_cl.c unix_sockets.c inet_sockets.c read_line.c)
target_link_libraries( is_seqnum_v2_cl lib )
ADD_EXECUTABLE( is_seqnum_v2_sv is_seqnum_v2_sv.c inet_sockets.c read_line.c unix_sockets.c)
target_link_libraries( is_seqnum_v2_sv lib )
ADD_EXECUTABLE( list_host_addresses list_host_addresses.c unix_sockets.c)
target_link_libraries( list_host_addresses lib )
ADD_EXECUTABLE( scm_cred_recv scm_cred_recv.c unix_sockets.c)
target_link_libraries( scm_cred_recv lib )
ADD_EXECUTABLE( scm_cred_send scm_cred_send.c unix_sockets.c)
target_link_libraries( scm_cred_send lib )
ADD_EXECUTABLE( scm_rights_recv scm_rights_recv.c unix_sockets.c)
target_link_libraries( scm_rights_recv lib )
ADD_EXECUTABLE( scm_rights_send scm_rights_send.c unix_sockets.c)
target_link_libraries( scm_rights_send lib )
ADD_EXECUTABLE( socknames socknames.c inet_sockets.c unix_sockets.c)
target_link_libraries( socknames lib )
ADD_EXECUTABLE( t_gethostbyname t_gethostbyname.c unix_sockets.c)
target_link_libraries( t_gethostbyname lib )
ADD_EXECUTABLE( t_getservbyname t_getservbyname.c unix_sockets.c)
target_link_libraries( t_getservbyname lib )
ADD_EXECUTABLE( ud_ucase_cl ud_ucase_cl.c unix_sockets.c)
target_link_libraries( ud_ucase_cl lib )
ADD_EXECUTABLE( ud_ucase_sv ud_ucase_sv.c unix_sockets.c)
target_link_libraries( ud_ucase_sv lib )
ADD_EXECUTABLE( us_abstract_bind us_abstract_bind.c unix_sockets.c)
target_link_libraries( us_abstract_bind lib )
ADD_EXECUTABLE( us_xfr_cl us_xfr_cl.c unix_sockets.c)
target_link_libraries( us_xfr_cl lib )
ADD_EXECUTABLE( us_xfr_sv us_xfr_sv.c unix_sockets.c)
target_link_libraries( us_xfr_sv lib )
ADD_EXECUTABLE( us_xfr_v2_cl us_xfr_v2_cl.c unix_sockets.c)
target_link_libraries( us_xfr_v2_cl lib )
ADD_EXECUTABLE( us_xfr_v2_sv us_xfr_v2_sv.c unix_sockets.c)
target_link_libraries( us_xfr_v2_sv lib )
ADD_EXECUTABLE( id_echo_sv id_echo_sv.c unix_sockets.c inet_sockets.c ${PROJECT_SOURCE_DIR}/daemons/become_daemon.c)
target_link_libraries( id_echo_sv lib )
ADD_EXECUTABLE( is_echo_sv is_echo_sv.c unix_sockets.c inet_sockets.c ${PROJECT_SOURCE_DIR}/daemons/become_daemon.c)
target_link_libraries( is_echo_sv lib )

include_directories(${PROJECT_SOURCE_DIR}/lib)


#install(TARGETS detached_attrib DESTINATION bin)
