set(Main_SRCS
   detached_attrib.c
   prod_no_condvar.c
   strerror.c
   strerror_tsd.c
   thread_incr.c
   thread_incr_spinlock.c
   one_time_init.c
   pthread_barrier_demo.c
   strerror_test.c
   thread_cancel.c
   thread_incr_mutex.c
   thread_lock_speed.c
   prod_condvar.c
   simple_thread.c
   strerror_tls.c
   thread_cleanup.c
   thread_incr_rwlock.c
   thread_multijoin.c
)

find_package( Threads )
ADD_EXECUTABLE(detached_attrib detached_attrib.c)
target_link_libraries(detached_attrib lib ${CMAKE_THREAD_LIBS_INIT} )

include_directories(${PROJECT_SOURCE_DIR}/lib)


install(TARGETS detached_attrib DESTINATION bin)
