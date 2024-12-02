./ns3

[ 79%] Linking CXX shared library /home/vikas/qkdnetsim-v2/build/lib/libns3.41-olsr-default.so
In file included from /home/vikas/qkdnetsim-v2/src/core/model/attribute.h:22,
                 from /home/vikas/qkdnetsim-v2/src/core/model/attribute-accessor-helper.h:22,
                 from /home/vikas/qkdnetsim-v2/src/core/model/attribute-helper.h:23,
                 from /home/vikas/qkdnetsim-v2/build/include/ns3/attribute-helper.h:1,
                 from /home/vikas/qkdnetsim-v2/src/network/model/address.h:25,
                 from /home/vikas/qkdnetsim-v2/build/include/ns3/address.h:1,
                 from /home/vikas/qkdnetsim-v2/src/applications/model/qkd-key-manager-system-application.cc:23:
In function ‘U* ns3::PeekPointer(const Ptr<T>&) [with U = Socket]’,
    inlined from ‘std::ostream& ns3::operator<<(std::ostream&, const Ptr<T>&) [with T = Socket]’ at /home/vikas/qkdnetsim-v2/src/core/model/ptr.h:466:22,
    inlined from ‘ns3::ParameterLogger& ns3::ParameterLogger::operator<<(const T&) [with T = ns3::Ptr<ns3::Socket>]’ at /home/vikas/qkdnetsim-v2/src/core/model/log.h:491:14,
    inlined from ‘ns3::Ptr<ns3::Socket> ns3::QKDKeyManagerSystemApplication::GetSocketFromHttp004AppQuery(ns3::UUID)’ at /home/vikas/qkdnetsim-v2/src/applications/model/qkd-key-manager-system-application.cc:3254:3:
/home/vikas/qkdnetsim-v2/src/core/model/ptr.h:451:14: warning: array subscript 0 is outside array bounds of ‘ns3::Ptr<ns3::Socket> [0]’ [-Warray-bounds=]
  451 |     return p.m_ptr;
      |              ^~~~~
In member function ‘ns3::Ptr<ns3::Socket> ns3::QKDKeyManagerSystemApplication::GetSocketFromHttp004AppQuery(ns3::UUID)’:
cc1plus: note: source object is likely at address zero
[ 79%] Linking CXX shared library /home/vikas/qkdnetsim-v2/build/lib/libns3.41-applications-default.so
