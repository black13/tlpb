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

ADD_EXECUTABLE(prod_no_condvar prod_no_condvar.c)
target_link_libraries(prod_no_condvar lib ${CMAKE_THREAD_LIBS_INIT} )

ADD_EXECUTABLE(thread_incr thread_incr.c)
target_link_libraries(thread_incr lib ${CMAKE_THREAD_LIBS_INIT} )

ADD_EXECUTABLE(thread_incr_spinlock thread_incr_spinlock.c)
target_link_libraries(thread_incr_spinlock lib ${CMAKE_THREAD_LIBS_INIT} )

ADD_EXECUTABLE(one_time_init one_time_init.c)
target_link_libraries(one_time_init lib ${CMAKE_THREAD_LIBS_INIT} )

ADD_EXECUTABLE(pthread_barrier_demo pthread_barrier_demo.c)
target_link_libraries(pthread_barrier_demo lib ${CMAKE_THREAD_LIBS_INIT} )

ADD_EXECUTABLE(strerror_test strerror_test.c)
target_link_libraries(strerror_test lib ${CMAKE_THREAD_LIBS_INIT} )

ADD_EXECUTABLE(thread_cancel thread_cancel.c)
target_link_libraries(thread_cancel lib ${CMAKE_THREAD_LIBS_INIT} )

ADD_EXECUTABLE(thread_incr_mutex thread_incr_mutex.c)
target_link_libraries(thread_incr_mutex lib ${CMAKE_THREAD_LIBS_INIT} )

ADD_EXECUTABLE(thread_lock_speed thread_lock_speed.c)
target_link_libraries(thread_lock_speed lib ${CMAKE_THREAD_LIBS_INIT} )

ADD_EXECUTABLE(prod_condvar prod_condvar.c)
target_link_libraries(prod_condvar lib ${CMAKE_THREAD_LIBS_INIT} )

ADD_EXECUTABLE(simple_thread simple_thread.c)
target_link_libraries(simple_thread lib ${CMAKE_THREAD_LIBS_INIT} )

#ADD_EXECUTABLE(strerror_tls strerror_tls.c)
#target_link_libraries(strerror_tls lib ${CMAKE_THREAD_LIBS_INIT} )

ADD_EXECUTABLE(thread_cleanup thread_cleanup.c)
target_link_libraries(thread_cleanup lib ${CMAKE_THREAD_LIBS_INIT} )

ADD_EXECUTABLE(thread_incr_rwlock thread_incr_rwlock.c)
target_link_libraries(thread_incr_rwlock lib ${CMAKE_THREAD_LIBS_INIT} )

ADD_EXECUTABLE(thread_multijoin thread_multijoin.c)
target_link_libraries(thread_multijoin lib ${CMAKE_THREAD_LIBS_INIT} )

include_directories(${PROJECT_SOURCE_DIR}/lib)


install(TARGETS detached_attrib DESTINATION bin)
