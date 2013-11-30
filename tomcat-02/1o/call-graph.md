**CGNode:** Node: < Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, main([Ljava/lang/String;)V > Context: ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,[Ljava/lang/String>@1 in Everywhere} ]
**IR:** < Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, main([Ljava/lang/String;)V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..3]
    -> BB2
    -> BB42
BB2[4..5]
    -> BB7
    -> BB3
BB3[6..8]
    -> BB4
    -> BB6
BB4[9..9]
    -> BB5
    -> BB6
    -> BB42
BB5[10..11]
    -> BB7
BB6[12..12]
    -> BB7
BB7[13..13]
    -> BB8
    -> BB42
BB8[14..17]
    -> BB9
    -> BB42
BB9[18..19]
    -> BB10
    -> BB42
BB10[20..22]
    -> BB11
    -> BB42
BB11[23..26]
    -> BB12
    -> BB42
BB12[27..28]
    -> BB13
    -> BB42
BB13[29..32]
    -> BB14
    -> BB42
BB14[33..34]
    -> BB15
    -> BB42
BB15[35..36]
    -> BB16
    -> BB42
BB16[37..38]
    -> BB17
    -> BB42
BB17[39..42]
    -> BB18
    -> BB42
BB18[43..44]
    -> BB19
    -> BB42
BB19[45..47]
    -> BB22
    -> BB20
BB20[48..50]
    -> BB21
    -> BB42
BB21[51..51]
    -> BB22
BB22[52..54]
    -> BB23
    -> BB42
BB23[55..58]
    -> BB26
    -> BB24
BB24[59..64]
    -> BB25
    -> BB42
BB25[65..66]
    -> BB26
    -> BB42
BB26[67..71]
    -> BB27
    -> BB42
BB27[72..74]
    -> BB28
    -> BB42
BB28[75..76]
    -> BB32
    -> BB29
BB29[77..77]
    -> BB30
    -> BB42
BB30[78..81]
    -> BB31
    -> BB42
BB31[82..82]
    -> BB32
BB32[83..85]
    -> BB33
    -> BB42
BB33[86..87]
    -> BB36
BB34[88..90]
    -> BB35
    -> BB42
BB35[91..95]
    -> BB36
BB36[96..98]
    -> BB37
    -> BB42
BB37[99..100]
    -> BB34
    -> BB38
BB38[101..112]
    -> BB39
    -> BB42
BB39[113..114]
    -> BB19
    -> BB40
BB40[115..120]
    -> BB41
    -> BB42
BB41[121..121]
    -> BB19
BB42[-1..-2]
Instructions:
BB0
BB1
3   v4 = arraylength v1                      (line 44)
BB2
5   conditional branch(le) v4,v5:#0          (line 44)
BB3
8   v6 = arrayload v1[v5:#0]                 (line 44)
BB4
9   v8 = invokestatic < Application, Ljava/lang/Integer, parseInt(Ljava/lang/String;)I > v6 @11 exception:v7(line 44)
BB5
11   goto                                    (line 44)
BB6<Handler>
           v9 = getCaughtException 
BB7
           v11 = phi  v3:#43800,v8,v3:#43800
13   v12 = new <Application,Lorg/apache/catalina/tribes/io/XByteBuffer>@19(line 45)
BB8
17   invokespecial < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, <init>(IZ)V > v12,v3:#43800,v13:#1 @26 exception:v14(line 45)
BB9
19   v15 = new <Application,Ljava/net/ServerSocket>@30(line 46)
BB10
22   invokespecial < Application, Ljava/net/ServerSocket, <init>(I)V > v15,v16:#9999 @37 exception:v17(line 46)
BB11
24   v18 = getstatic < Application, Ljava/lang/System, out, <Application,Ljava/io/PrintStream> >(line 47)
26   invokevirtual < Application, Ljava/io/PrintStream, println(Ljava/lang/String;)V > v18,v19:#Listening on 9999 @46 exception:v20(line 47)
BB12
28   v22 = invokevirtual < Application, Ljava/net/ServerSocket, accept()Ljava/net/Socket; > v15 @50 exception:v21(line 48)
BB13
32   invokevirtual < Application, Ljava/net/Socket, setReceiveBufferSize(I)V > v22,v11 @58 exception:v23(line 49)
BB14
34   v25 = invokevirtual < Application, Ljava/net/Socket, getInputStream()Ljava/io/InputStream; > v22 @63 exception:v24(line 50)
BB15
36   v26 = new <Application,Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive$1>@68(line 51)
BB16
38   invokespecial < Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive$1, <init>()V > v26 @72 exception:v27(line 51)
BB17
42   invokevirtual < Application, Ljava/lang/Thread, setDaemon(Z)V > v26,v13:#1 @80 exception:v28(line 62)
BB18
44   invokevirtual < Application, Ljava/lang/Thread, start()V > v26 @85 exception:v29(line 63)
BB19
45   v30 = getstatic < Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, first, <Primordial,Z> >(line 66)
47   conditional branch(eq) v30,v5:#0        (line 66)
BB20
49   putstatic v5:#0 < Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, first, <Primordial,Z> >(line 66)
50   v32 = invokestatic < Application, Ljava/lang/System, currentTimeMillis()J > @98 exception:v31(line 66)
BB21
51   putstatic v32 < Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, start, <Primordial,J> >(line 66)
BB22
53   v33 = getstatic < Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, buf, <Primordial,[B> >(line 67)
54   v35 = invokevirtual < Application, Ljava/io/InputStream, read([B)I > v25,v33 @109 exception:v34(line 67)
BB23
58   conditional branch(ne) v35,v36:#-1      (line 68)
BB24
59   v37 = getstatic < Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, start, <Primordial,J> >(line 69)
60   v38 = getstatic < Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, mb, <Primordial,D> >(line 69)
61   v39 = getstatic < Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, count, <Primordial,I> >(line 69)
62   v40 = getstatic < Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, df, <Application,Ljava/text/DecimalFormat> >(line 69)
63   v41 = getstatic < Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, total, <Application,Ljava/math/BigDecimal> >(line 69)
64   invokestatic < Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, printStats(JDILjava/text/DecimalFormat;Ljava/math/BigDecimal;)V > v37,v38,v39,v40,v41 @135 exception:v42(line 69)
BB25
66   invokestatic < Application, Ljava/lang/System, exit(I)V > v13:#1 @139 exception:v43(line 70)
BB26
68   v44 = getstatic < Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, buf, <Primordial,[B> >(line 72)
71   v46 = invokevirtual < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, append([BII)Z > v12,v44,v5:#0,v35 @149 exception:v45(line 72)
BB27
73   v47 = getstatic < Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, bytes, <Application,Ljava/math/BigDecimal> >(line 73)
74   v49 = invokevirtual < Application, Ljava/math/BigDecimal, intValue()I > v47 @156 exception:v48(line 73)
BB28
76   conditional branch(eq) v49,v35          (line 73)
BB29
77   v50 = new <Application,Ljava/math/BigDecimal>@164(line 73)
BB30
80   v51 = conversion(D) v35                 (line 73)
81   invokespecial < Application, Ljava/math/BigDecimal, <init>(D)V > v50,v51 @171 exception:v52(line 73)
BB31
82   putstatic v50 < Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, bytes, <Application,Ljava/math/BigDecimal> >(line 73)
BB32
83   v53 = getstatic < Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, total, <Application,Ljava/math/BigDecimal> >(line 74)
84   v54 = getstatic < Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, bytes, <Application,Ljava/math/BigDecimal> >(line 74)
85   v56 = invokevirtual < Application, Ljava/math/BigDecimal, add(Ljava/math/BigDecimal;)Ljava/math/BigDecimal; > v53,v54 @183 exception:v55(line 74)
BB33
86   putstatic v56 < Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, total, <Application,Ljava/math/BigDecimal> >(line 74)
87   goto                                    (line 75)
BB34
90   v60 = invokevirtual < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, extractPackage(Z)Lorg/apache/catalina/tribes/io/ChannelData; > v12,v13:#1 @194 exception:v59(line 76)
BB35
92   v61 = getstatic < Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, count, <Primordial,I> >(line 77)
94   v62 = binaryop(add) v61 , v13:#1        (line 77)
95   putstatic v62 < Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, count, <Primordial,I> >(line 77)
BB36
98   v58 = invokevirtual < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, countPackages(Z)I > v12,v13:#1 @208 exception:v57(line 75)
BB37
100   conditional branch(gt) v58,v5:#0       (line 75)
BB38
101   v63 = getstatic < Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, mb, <Primordial,D> >(line 79)
103   v64 = conversion(D) v35                (line 79)
105   v66 = binaryop(div) v64 , v65:#1024.0  (line 79)
107   v67 = binaryop(div) v66 , v65:#1024.0  (line 79)
108   v68 = binaryop(add) v63 , v67          (line 79)
109   putstatic v68 < Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, mb, <Primordial,D> >(line 79)
110   v69 = getstatic < Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, count, <Primordial,I> >(line 80)
112   v71 = binaryop(rem) v69 , v70:#10000   (line 80)
BB39
114   conditional branch(ne) v71,v5:#0       (line 80)
BB40
115   v72 = getstatic < Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, start, <Primordial,J> >(line 81)
116   v73 = getstatic < Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, mb, <Primordial,D> >(line 81)
117   v74 = getstatic < Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, count, <Primordial,I> >(line 81)
118   v75 = getstatic < Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, df, <Application,Ljava/text/DecimalFormat> >(line 81)
119   v76 = getstatic < Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, total, <Application,Ljava/math/BigDecimal> >(line 81)
120   invokestatic < Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, printStats(JDILjava/text/DecimalFormat;Ljava/math/BigDecimal;)V > v72,v73,v74,v75,v76 @257 exception:v77(line 81)
BB41
121   goto                                   (line 65)
BB42

**CGNode:** Node: < Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, <clinit>()V > Context: Everywhere
**IR:** < Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, <clinit>()V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..5]
    -> BB2
    -> BB9
BB2[6..11]
    -> BB3
    -> BB9
BB3[12..14]
    -> BB4
    -> BB9
BB4[15..16]
    -> BB5
    -> BB9
BB5[17..19]
    -> BB6
    -> BB9
BB6[20..21]
    -> BB7
    -> BB9
BB7[22..24]
    -> BB8
    -> BB9
BB8[25..26]
    -> BB9
BB9[-1..-2]
Instructions:
BB0
BB1
1   putstatic v2:#0 < Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, start, <Primordial,J> >(line 30)
3   putstatic v3:#0.0 < Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, mb, <Primordial,D> >(line 31)
5   v5 = new <Primordial,[B>@10v4:#32871     (line 33)
BB2
6   putstatic v5 < Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, buf, <Primordial,[B> >(line 33)
8   putstatic v6:#1 < Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, first, <Primordial,Z> >(line 34)
10   putstatic v7:#0 < Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, count, <Primordial,I> >(line 35)
11   v8 = new <Application,Ljava/text/DecimalFormat>@23(line 36)
BB3
14   invokespecial < Application, Ljava/text/DecimalFormat, <init>(Ljava/lang/String;)V > v8,v9:###.00 @29 exception:v10(line 36)
BB4
15   putstatic v8 < Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, df, <Application,Ljava/text/DecimalFormat> >(line 36)
16   v11 = new <Application,Ljava/math/BigDecimal>@35(line 37)
BB5
19   invokespecial < Application, Ljava/math/BigDecimal, <init>(D)V > v11,v3:#0.0 @40 exception:v12(line 37)
BB6
20   putstatic v11 < Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, total, <Application,Ljava/math/BigDecimal> >(line 37)
21   v13 = new <Application,Ljava/math/BigDecimal>@46(line 38)
BB7
24   invokespecial < Application, Ljava/math/BigDecimal, <init>(D)V > v13,v14:#32871.0 @53 exception:v15(line 38)
BB8
25   putstatic v13 < Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, bytes, <Application,Ljava/math/BigDecimal> >(line 38)
26   return                                  (line 29)
BB9

**CGNode:** Node: < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, main([Ljava/lang/String;)V > Context: ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,[Ljava/lang/String>@6 in Everywhere} ]
**IR:** < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, main([Ljava/lang/String;)V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..0]
    -> BB2
    -> BB5
BB2[1..2]
    -> BB3
    -> BB5
BB3[3..3]
    -> BB4
    -> BB5
BB4[4..4]
    -> BB5
BB5[-1..-2]
Instructions:
BB0
BB1
0   v3 = new <Application,Lorg/apache/tomcat/util/net/AprEndpoint>@0(line 583)
BB2
2   invokespecial < Application, Lorg/apache/tomcat/util/net/AprEndpoint, <init>()V > v3 @4 exception:v4(line 583)
BB3
3   invokevirtual < Application, Lorg/apache/tomcat/util/net/AprEndpoint, startAcceptorThreads()V > v3 @7 exception:v5(line 583)
BB4
4   return                                   (line 584)
BB5

**CGNode:** Node: < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, <clinit>()V > Context: Everywhere
**IR:** < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, <clinit>()V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..1]
    -> BB2
    -> BB3
BB2[2..3]
    -> BB3
BB3[-1..-2]
Instructions:
BB0
BB1
1   v4 = invokestatic < Application, Lorg/apache/tomcat/util/res/StringManager, getManager(Ljava/lang/String;)Lorg/apache/tomcat/util/res/StringManager; > v2:#org.apache.tomcat.util.net.res @2 exception:v3(line 51)
BB2
2   putstatic v4 < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, sm, <Application,Lorg/apache/tomcat/util/res/StringManager> >(line 51)
3   return                                   (line 48)
BB3

**CGNode:** Node: < Application, Lorg/apache/catalina/tribes/group/interceptors/MessageDispatchInterceptor, <clinit>()V > Context: Everywhere
**IR:** < Application, Lorg/apache/catalina/tribes/group/interceptors/MessageDispatchInterceptor, <clinit>()V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..0]
    -> BB2
    -> BB4
BB2[1..1]
    -> BB3
    -> BB4
BB3[2..3]
    -> BB4
BB4[-1..-2]
Instructions:
BB0
BB1
0   v2 = load_metadata: <Primordial,Lorg/apache/catalina/tribes/group/interceptors/MessageDispatchInterceptor>, <Primordial,Ljava/lang/Class>(line 46)
BB2
1   v4 = invokestatic < Application, Lorg/apache/juli/logging/LogFactory, getLog(Ljava/lang/Class;)Lorg/apache/juli/logging/Log; > v2 @2 exception:v3(line 46)
BB3
2   putstatic v4 < Application, Lorg/apache/catalina/tribes/group/interceptors/MessageDispatchInterceptor, log, <Application,Lorg/apache/juli/logging/Log> >(line 46)
3   return                                   (line 45)
BB4

**CGNode:** Node: < Application, Lorg/apache/catalina/tribes/group/interceptors/MessageDispatchInterceptor, <init>()V > Context: ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,Lorg/apache/catalina/tribes/group/interceptors/MessageDispatchInterceptor>@11 in Everywhere} ]
**IR:** < Application, Lorg/apache/catalina/tribes/group/interceptors/MessageDispatchInterceptor, <init>()V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..1]
    -> BB2
    -> BB13
BB2[2..4]
    -> BB3
    -> BB13
BB3[5..6]
    -> BB4
    -> BB13
BB4[7..8]
    -> BB5
    -> BB13
BB5[9..9]
    -> BB6
    -> BB13
BB6[10..12]
    -> BB7
    -> BB13
BB7[13..15]
    -> BB8
    -> BB13
BB8[16..18]
    -> BB9
    -> BB13
BB9[19..21]
    -> BB10
    -> BB13
BB10[22..24]
    -> BB11
    -> BB13
BB11[25..27]
    -> BB12
    -> BB13
BB12[28..28]
    -> BB13
BB13[-1..-2]
Instructions:
BB0
BB1
1   invokespecial < Application, Lorg/apache/catalina/tribes/group/ChannelInterceptorBase, <init>()V > v1 @1 exception:v3(line 56)
BB2
4   putfield v1 = v4:#67108864 < Application, Lorg/apache/catalina/tribes/group/interceptors/MessageDispatchInterceptor, maxQueueSize, <Primordial,J> >(line 48)
BB3
6   v5 = new <Application,Lorg/apache/catalina/tribes/transport/bio/util/FastQueue>@12(line 49)
BB4
8   invokespecial < Application, Lorg/apache/catalina/tribes/transport/bio/util/FastQueue, <init>()V > v5 @16 exception:v6(line 49)
BB5
9   putfield v1 = v5 < Application, Lorg/apache/catalina/tribes/group/interceptors/MessageDispatchInterceptor, queue, <Application,Lorg/apache/catalina/tribes/transport/bio/util/FastQueue> >(line 49)
BB6
12   putfield v1 = v7:#0 < Application, Lorg/apache/catalina/tribes/group/interceptors/MessageDispatchInterceptor, run, <Primordial,Z> >(line 50)
BB7
15   putfield v1 = v8:#null < Application, Lorg/apache/catalina/tribes/group/interceptors/MessageDispatchInterceptor, msgDispatchThread, <Application,Ljava/lang/Thread> >(line 51)
BB8
18   putfield v1 = v9:#0 < Application, Lorg/apache/catalina/tribes/group/interceptors/MessageDispatchInterceptor, currentSize, <Primordial,J> >(line 52)
BB9
21   putfield v1 = v10:#1 < Application, Lorg/apache/catalina/tribes/group/interceptors/MessageDispatchInterceptor, useDeepClone, <Primordial,Z> >(line 53)
BB10
24   putfield v1 = v10:#1 < Application, Lorg/apache/catalina/tribes/group/interceptors/MessageDispatchInterceptor, alwaysSend, <Primordial,Z> >(line 54)
BB11
27   invokevirtual < Application, Lorg/apache/catalina/tribes/group/interceptors/MessageDispatchInterceptor, setOptionFlag(I)V > v1,v11:#8 @50 exception:v12(line 57)
BB12
28   return                                  (line 58)
BB13

**CGNode:** Node: < Application, Lorg/apache/catalina/tribes/group/interceptors/MessageDispatchInterceptor, run()V > Context: ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,Lorg/apache/catalina/tribes/group/interceptors/MessageDispatchInterceptor>@11 in Everywhere} ]
**IR:** < Application, Lorg/apache/catalina/tribes/group/interceptors/MessageDispatchInterceptor, run()V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..0]
    -> BB10
BB2[1..2]
    -> BB3
    -> BB13
BB3[3..6]
    -> BB7
    -> BB4
BB4[7..7]
    -> BB10
BB5[8..10]
    -> BB6
    -> BB13
BB6[11..11]
    -> BB7
BB7[12..14]
    -> BB10
    -> BB8
BB8[15..16]
    -> BB9
    -> BB13
BB9[17..18]
    -> BB5
    -> BB10
BB10[19..20]
    -> BB11
    -> BB13
BB11[21..22]
    -> BB2
    -> BB12
BB12[23..23]
    -> BB13
BB13[-1..-2]
Instructions:
BB0
BB1
0   goto                                     (line 180)
BB2
2   v6 = invokevirtual < Application, Lorg/apache/catalina/tribes/group/interceptors/MessageDispatchInterceptor, removeFromQueue()Lorg/apache/catalina/tribes/transport/bio/util/LinkObject; > v1 @4 exception:v5(line 181)
BB3
6   conditional branch(ne) v6,v7:#null       (line 182)
BB4
7   goto                                     (line 182)
BB5
10   v10 = invokevirtual < Application, Lorg/apache/catalina/tribes/group/interceptors/MessageDispatchInterceptor, sendAsyncData(Lorg/apache/catalina/tribes/transport/bio/util/LinkObject;)Lorg/apache/catalina/tribes/transport/bio/util/LinkObject; > v1,v11 @17 exception:v9(line 184)
BB6
BB7
           v11 = phi  v6,v10
14   conditional branch(eq) v11,v7:#null     (line 183)
BB8
16   v8 = getfield < Application, Lorg/apache/catalina/tribes/group/interceptors/MessageDispatchInterceptor, run, <Primordial,Z> > v1(line 183)
BB9
18   conditional branch(ne) v8,v4:#0         (line 183)
BB10
20   v3 = getfield < Application, Lorg/apache/catalina/tribes/group/interceptors/MessageDispatchInterceptor, run, <Primordial,Z> > v1(line 180)
BB11
22   conditional branch(ne) v3,v4:#0         (line 180)
BB12
23   return                                  (line 187)
BB13

**CGNode:** Node: < Application, Lorg/apache/tomcat/util/net/NioBlockingSelector$BlockPoller, <init>()V > Context: ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,Lorg/apache/tomcat/util/net/NioBlockingSelector$BlockPoller>@14 in Everywhere} ]
**IR:** < Application, Lorg/apache/tomcat/util/net/NioBlockingSelector$BlockPoller, <init>()V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..1]
    -> BB2
    -> BB11
BB2[2..4]
    -> BB3
    -> BB11
BB3[5..7]
    -> BB4
    -> BB11
BB4[8..9]
    -> BB5
    -> BB11
BB5[10..11]
    -> BB6
    -> BB11
BB6[12..12]
    -> BB7
    -> BB11
BB7[13..14]
    -> BB8
    -> BB11
BB8[15..17]
    -> BB9
    -> BB11
BB9[18..18]
    -> BB10
    -> BB11
BB10[19..19]
    -> BB11
BB11[-1..-2]
Instructions:
BB0
BB1
1   invokespecial < Application, Ljava/lang/Thread, <init>()V > v1 @1 exception:v3(line 205)
BB2
4   putfield v1 = v4:#1 < Application, Lorg/apache/tomcat/util/net/NioBlockingSelector$BlockPoller, run, <Primordial,Z> >(line 206)
BB3
7   putfield v1 = v5:#null < Application, Lorg/apache/tomcat/util/net/NioBlockingSelector$BlockPoller, selector, <Application,Ljava/nio/channels/Selector> >(line 207)
BB4
9   v6 = new <Application,Ljava/util/concurrent/ConcurrentLinkedQueue>@15(line 208)
BB5
11   invokespecial < Application, Ljava/util/concurrent/ConcurrentLinkedQueue, <init>()V > v6 @19 exception:v7(line 208)
BB6
12   putfield v1 = v6 < Application, Lorg/apache/tomcat/util/net/NioBlockingSelector$BlockPoller, events, <Application,Ljava/util/concurrent/ConcurrentLinkedQueue> >(line 208)
BB7
14   v8 = new <Application,Ljava/util/concurrent/atomic/AtomicInteger>@26(line 210)
BB8
17   invokespecial < Application, Ljava/util/concurrent/atomic/AtomicInteger, <init>(I)V > v8,v9:#0 @31 exception:v10(line 210)
BB9
18   putfield v1 = v8 < Application, Lorg/apache/tomcat/util/net/NioBlockingSelector$BlockPoller, wakeupCounter, <Application,Ljava/util/concurrent/atomic/AtomicInteger> >(line 210)
BB10
19   return                                  (line 205)
BB11

**CGNode:** Node: < Application, Lorg/apache/tomcat/util/net/NioBlockingSelector$BlockPoller, run()V > Context: ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,Lorg/apache/tomcat/util/net/NioBlockingSelector$BlockPoller>@14 in Everywhere} ]
**IR:** < Application, Lorg/apache/tomcat/util/net/NioBlockingSelector$BlockPoller, run()V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..0]
    -> BB76
BB2[1..2]
    -> BB3
    -> BB74
BB3[3..7]
    -> BB4
    -> BB19
BB4[8..8]
    -> BB5
    -> BB19
    -> BB28
    -> BB34
BB5[9..12]
    -> BB9
    -> BB6
BB6[13..14]
    -> BB7
    -> BB19
BB7[15..15]
    -> BB8
    -> BB19
    -> BB28
    -> BB34
BB8[16..17]
    -> BB14
BB9[18..19]
    -> BB10
    -> BB19
BB10[20..21]
    -> BB11
    -> BB19
    -> BB28
    -> BB34
BB11[22..23]
    -> BB12
    -> BB19
BB12[24..25]
    -> BB13
    -> BB19
    -> BB28
    -> BB34
BB13[26..26]
    -> BB14
BB14[27..28]
    -> BB15
    -> BB19
BB15[29..30]
    -> BB16
    -> BB19
    -> BB28
    -> BB34
BB16[31..32]
    -> BB17
    -> BB19
BB17[33..34]
    -> BB38
    -> BB18
BB18[35..35]
    -> BB78
BB19[36..38]
    -> BB20
    -> BB74
BB20[39..40]
    -> BB22
    -> BB21
BB21[41..42]
    -> BB74
    -> BB97
BB22[43..43]
    -> BB23
    -> BB74
BB23[44..44]
    -> BB24
    -> BB74
BB24[45..46]
    -> BB76
    -> BB25
BB25[47..47]
    -> BB26
    -> BB74
BB26[48..50]
    -> BB27
    -> BB74
BB27[51..51]
    -> BB76
BB28[52..53]
    -> BB29
    -> BB74
BB29[54..54]
    -> BB30
    -> BB74
BB30[55..56]
    -> BB76
    -> BB31
BB31[57..57]
    -> BB32
    -> BB74
BB32[58..60]
    -> BB33
    -> BB74
BB33[61..61]
    -> BB76
BB34[62..64]
    -> BB35
    -> BB74
BB35[65..65]
    -> BB36
    -> BB74
BB36[66..68]
    -> BB37
    -> BB74
BB37[69..69]
    -> BB76
BB38[70..72]
    -> BB43
    -> BB39
BB39[73..74]
    -> BB40
    -> BB74
BB40[75..75]
    -> BB41
    -> BB74
BB41[76..76]
    -> BB42
    -> BB74
BB42[77..77]
    -> BB44
BB43[78..78]
    -> BB44
BB44[79..80]
    -> BB68
BB45[81..82]
    -> BB46
    -> BB74
BB46[83..83]
    -> BB47
    -> BB74
BB47[84..86]
    -> BB48
    -> BB74
BB48[87..87]
    -> BB49
    -> BB74
BB49[88..90]
    -> BB50
    -> BB63
    -> BB74
BB50[91..92]
    -> BB51
    -> BB63
    -> BB74
BB51[93..95]
    -> BB52
    -> BB63
    -> BB74
BB52[96..97]
    -> BB53
    -> BB63
    -> BB74
BB53[98..101]
    -> BB54
    -> BB63
    -> BB74
BB54[102..104]
    -> BB55
    -> BB63
    -> BB74
BB55[105..106]
    -> BB58
    -> BB56
BB56[107..109]
    -> BB57
    -> BB63
    -> BB74
BB57[110..110]
    -> BB58
    -> BB63
    -> BB74
BB58[111..112]
    -> BB59
    -> BB63
    -> BB74
BB59[113..114]
    -> BB68
    -> BB60
BB60[115..117]
    -> BB61
    -> BB63
    -> BB74
BB61[118..118]
    -> BB62
    -> BB63
    -> BB74
BB62[119..119]
    -> BB68
BB63[120..122]
    -> BB64
    -> BB74
BB64[123..125]
    -> BB65
    -> BB74
BB65[126..126]
    -> BB66
    -> BB74
BB66[127..129]
    -> BB67
    -> BB74
BB67[130..130]
    -> BB68
    -> BB74
BB68[131..132]
    -> BB69
    -> BB74
BB69[133..134]
    -> BB76
    -> BB70
BB70[135..137]
    -> BB76
    -> BB71
BB71[138..139]
    -> BB72
    -> BB74
BB72[140..141]
    -> BB45
    -> BB73
BB73[142..142]
    -> BB76
BB74[143..144]
    -> BB75
    -> BB97
BB75[145..147]
    -> BB76
    -> BB97
BB76[148..149]
    -> BB77
    -> BB97
BB77[150..151]
    -> BB2
    -> BB78
BB78[152..153]
    -> BB79
    -> BB97
BB79[154..154]
    -> BB80
    -> BB97
BB80[155..156]
    -> BB81
    -> BB83
BB81[157..157]
    -> BB82
    -> BB83
    -> BB97
BB82[158..159]
    -> BB88
BB83[160..161]
    -> BB84
    -> BB97
BB84[162..162]
    -> BB85
    -> BB97
BB85[163..164]
    -> BB88
    -> BB86
BB86[165..165]
    -> BB87
    -> BB97
BB87[166..168]
    -> BB88
    -> BB97
BB88[169..170]
    -> BB89
    -> BB91
BB89[171..171]
    -> BB90
    -> BB91
    -> BB97
BB90[172..172]
    -> BB96
BB91[173..174]
    -> BB92
    -> BB97
BB92[175..175]
    -> BB93
    -> BB97
BB93[176..177]
    -> BB96
    -> BB94
BB94[178..178]
    -> BB95
    -> BB97
BB95[179..181]
    -> BB96
    -> BB97
BB96[182..182]
    -> BB97
BB97[-1..-2]
Instructions:
BB0
BB1
0   goto                                     (line 320)
BB2
2   v6 = invokevirtual < Application, Lorg/apache/tomcat/util/net/NioBlockingSelector$BlockPoller, events()Z > v1 @4 exception:v5(line 322)
BB3
7   v7 = getfield < Application, Lorg/apache/tomcat/util/net/NioBlockingSelector$BlockPoller, wakeupCounter, <Application,Ljava/util/concurrent/atomic/AtomicInteger> > v1(line 325)
BB4
8   v9 = invokevirtual < Application, Ljava/util/concurrent/atomic/AtomicInteger, get()I > v7 @14 exception:v8(line 325)
BB5
12   conditional branch(le) v9,v4:#0         (line 326)
BB6
14   v10 = getfield < Application, Lorg/apache/tomcat/util/net/NioBlockingSelector$BlockPoller, selector, <Application,Ljava/nio/channels/Selector> > v1(line 327)
BB7
15   v12 = invokevirtual < Application, Ljava/nio/channels/Selector, selectNow()I > v10 @26 exception:v11(line 327)
BB8
17   goto                                    (line 327)
BB9
19   v13 = getfield < Application, Lorg/apache/tomcat/util/net/NioBlockingSelector$BlockPoller, wakeupCounter, <Application,Ljava/util/concurrent/atomic/AtomicInteger> > v1(line 329)
BB10
21   invokevirtual < Application, Ljava/util/concurrent/atomic/AtomicInteger, set(I)V > v13,v14:#-1 @38 exception:v15(line 329)
BB11
23   v16 = getfield < Application, Lorg/apache/tomcat/util/net/NioBlockingSelector$BlockPoller, selector, <Application,Ljava/nio/channels/Selector> > v1(line 330)
BB12
25   v19 = invokevirtual < Application, Ljava/nio/channels/Selector, select(J)I > v16,v17:#1000 @48 exception:v18(line 330)
BB13
BB14
           v20 = phi  v12,v19
28   v21 = getfield < Application, Lorg/apache/tomcat/util/net/NioBlockingSelector$BlockPoller, wakeupCounter, <Application,Ljava/util/concurrent/atomic/AtomicInteger> > v1(line 332)
BB15
30   invokevirtual < Application, Ljava/util/concurrent/atomic/AtomicInteger, set(I)V > v21,v4:#0 @57 exception:v22(line 332)
BB16
32   v23 = getfield < Application, Lorg/apache/tomcat/util/net/NioBlockingSelector$BlockPoller, run, <Primordial,Z> > v1(line 333)
BB17
34   conditional branch(ne) v23,v4:#0        (line 333)
BB18
35   goto                                    (line 333)
BB19<Handler>
           v24 = getCaughtException 
38   v26 = getfield < Application, Lorg/apache/tomcat/util/net/NioBlockingSelector$BlockPoller, selector, <Application,Ljava/nio/channels/Selector> > v1(line 336)
BB20
40   conditional branch(ne) v26,v27:#null    (line 336)
BB21
42   throw v24                               (line 336)
BB22
43   v29 = invokestatic < Application, Lorg/apache/tomcat/util/net/NioBlockingSelector, access$0()Lorg/apache/juli/logging/Log; > @80 exception:v28(line 337)
BB23
44   v31 = invokeinterface < Application, Lorg/apache/juli/logging/Log, isDebugEnabled()Z > v29 @83 exception:v30(line 337)
BB24
46   conditional branch(eq) v31,v4:#0        (line 337)
BB25
47   v88 = invokestatic < Application, Lorg/apache/tomcat/util/net/NioBlockingSelector, access$0()Lorg/apache/juli/logging/Log; > @91 exception:v87(line 337)
BB26
50   invokeinterface < Application, Lorg/apache/juli/logging/Log, debug(Ljava/lang/Object;Ljava/lang/Throwable;)V > v88,v89:#Possibly encountered sun bug 5076772 on windows JDK 1.5,v24 @97 exception:v90(line 337)
BB27
51   goto                                    (line 338)
BB28<Handler>
           v34 = getCaughtException 
53   v38 = invokestatic < Application, Lorg/apache/tomcat/util/net/NioBlockingSelector, access$0()Lorg/apache/juli/logging/Log; > @106 exception:v37(line 341)
BB29
54   v40 = invokeinterface < Application, Lorg/apache/juli/logging/Log, isDebugEnabled()Z > v38 @109 exception:v39(line 341)
BB30
56   conditional branch(eq) v40,v4:#0        (line 341)
BB31
57   v92 = invokestatic < Application, Lorg/apache/tomcat/util/net/NioBlockingSelector, access$0()Lorg/apache/juli/logging/Log; > @117 exception:v91(line 341)
BB32
60   invokeinterface < Application, Lorg/apache/juli/logging/Log, debug(Ljava/lang/Object;Ljava/lang/Throwable;)V > v92,v89:#Possibly encountered sun bug 5076772 on windows JDK 1.5,v34 @123 exception:v93(line 341)
BB33
61   goto                                    (line 342)
BB34<Handler>
           v94 = getCaughtException 
64   invokestatic < Application, Lorg/apache/tomcat/util/ExceptionUtils, handleThrowable(Ljava/lang/Throwable;)V > v94 @133 exception:v97(line 344)
BB35
65   v99 = invokestatic < Application, Lorg/apache/tomcat/util/net/NioBlockingSelector, access$0()Lorg/apache/juli/logging/Log; > @136 exception:v98(line 345)
BB36
68   invokeinterface < Application, Lorg/apache/juli/logging/Log, error(Ljava/lang/Object;Ljava/lang/Throwable;)V > v99,v100:#,v94 @142 exception:v101(line 345)
BB37
69   goto                                    (line 346)
BB38
72   conditional branch(le) v20,v4:#0        (line 349)
BB39
74   v43 = getfield < Application, Lorg/apache/tomcat/util/net/NioBlockingSelector$BlockPoller, selector, <Application,Ljava/nio/channels/Selector> > v1(line 349)
BB40
75   v45 = invokevirtual < Application, Ljava/nio/channels/Selector, selectedKeys()Ljava/util/Set; > v43 @158 exception:v44(line 349)
BB41
76   v47 = invokeinterface < Application, Ljava/util/Set, iterator()Ljava/util/Iterator; > v45 @161 exception:v46(line 349)
BB42
77   goto                                    (line 349)
BB43
BB44
           v48 = phi  v47,v27:#null
80   goto                                    (line 353)
BB45
82   v53 = invokeinterface < Application, Ljava/util/Iterator, next()Ljava/lang/Object; > v48 @175 exception:v52(line 354)
BB46
83   v54 = checkcast <Application,Ljava/nio/channels/SelectionKey>v53(line 354)
BB47
86   v56 = invokevirtual < Application, Ljava/nio/channels/SelectionKey, attachment()Ljava/lang/Object; > v54 @185 exception:v55(line 355)
BB48
87   v57 = checkcast <Application,Lorg/apache/tomcat/util/net/NioEndpoint$KeyAttachment>v56(line 355)
BB49
90   invokevirtual < Application, Lorg/apache/tomcat/util/net/NioEndpoint$KeyAttachment, access()V > v57 @195 exception:v58(line 357)
BB50
92   invokeinterface < Application, Ljava/util/Iterator, remove()V > v48 @199 exception:v59(line 358)
BB51
95   v61 = invokevirtual < Application, Ljava/nio/channels/SelectionKey, interestOps()I > v54 @206 exception:v60(line 359)
BB52
97   v63 = invokevirtual < Application, Ljava/nio/channels/SelectionKey, readyOps()I > v54 @210 exception:v62(line 359)
BB53
99   v64 = binaryop(xor) v63 , v14:#-1       (line 359)
100   v65 = binaryop(and) v61 , v64          (line 359)
101   v67 = invokevirtual < Application, Ljava/nio/channels/SelectionKey, interestOps(I)Ljava/nio/channels/SelectionKey; > v54,v65 @216 exception:v66(line 359)
BB54
104   v69 = invokevirtual < Application, Ljava/nio/channels/SelectionKey, isReadable()Z > v54 @221 exception:v68(line 360)
BB55
106   conditional branch(eq) v69,v4:#0       (line 360)
BB56
109   v71 = invokevirtual < Application, Lorg/apache/tomcat/util/net/NioEndpoint$KeyAttachment, getReadLatch()Ljava/util/concurrent/CountDownLatch; > v57 @230 exception:v70(line 361)
BB57
110   invokevirtual < Application, Lorg/apache/tomcat/util/net/NioBlockingSelector$BlockPoller, countDown(Ljava/util/concurrent/CountDownLatch;)V > v1,v71 @233 exception:v72(line 361)
BB58
112   v74 = invokevirtual < Application, Ljava/nio/channels/SelectionKey, isWritable()Z > v54 @237 exception:v73(line 363)
BB59
114   conditional branch(eq) v74,v4:#0       (line 363)
BB60
117   v76 = invokevirtual < Application, Lorg/apache/tomcat/util/net/NioEndpoint$KeyAttachment, getWriteLatch()Ljava/util/concurrent/CountDownLatch; > v57 @246 exception:v75(line 364)
BB61
118   invokevirtual < Application, Lorg/apache/tomcat/util/net/NioBlockingSelector$BlockPoller, countDown(Ljava/util/concurrent/CountDownLatch;)V > v1,v76 @249 exception:v77(line 364)
BB62
119   goto                                   (line 364)
BB63<Handler>
           v78 = getCaughtException 
122   invokevirtual < Application, Ljava/nio/channels/SelectionKey, cancel()V > v54 @258 exception:v79(line 367)
BB64
125   v81 = invokevirtual < Application, Lorg/apache/tomcat/util/net/NioEndpoint$KeyAttachment, getReadLatch()Ljava/util/concurrent/CountDownLatch; > v57 @264 exception:v80(line 368)
BB65
126   invokevirtual < Application, Lorg/apache/tomcat/util/net/NioBlockingSelector$BlockPoller, countDown(Ljava/util/concurrent/CountDownLatch;)V > v1,v81 @267 exception:v82(line 368)
BB66
129   v84 = invokevirtual < Application, Lorg/apache/tomcat/util/net/NioEndpoint$KeyAttachment, getWriteLatch()Ljava/util/concurrent/CountDownLatch; > v57 @273 exception:v83(line 369)
BB67
130   invokevirtual < Application, Lorg/apache/tomcat/util/net/NioBlockingSelector$BlockPoller, countDown(Ljava/util/concurrent/CountDownLatch;)V > v1,v84 @276 exception:v85(line 369)
BB68
132   v49 = getfield < Application, Lorg/apache/tomcat/util/net/NioBlockingSelector$BlockPoller, run, <Primordial,Z> > v1(line 353)
BB69
134   conditional branch(eq) v49,v4:#0       (line 353)
BB70
137   conditional branch(eq) v48,v27:#null   (line 353)
BB71
139   v51 = invokeinterface < Application, Ljava/util/Iterator, hasNext()Z > v48 @291 exception:v50(line 353)
BB72
141   conditional branch(ne) v51,v4:#0       (line 353)
BB73
142   goto                                   (line 353)
BB74<Handler>
           v102 = getCaughtException 
144   v106 = invokestatic < Application, Lorg/apache/tomcat/util/net/NioBlockingSelector, access$0()Lorg/apache/juli/logging/Log; > @303 exception:v105(line 373)
BB75
147   invokeinterface < Application, Lorg/apache/juli/logging/Log, error(Ljava/lang/Object;Ljava/lang/Throwable;)V > v106,v100:#,v102 @309 exception:v107(line 373)
BB76
149   v3 = getfield < Application, Lorg/apache/tomcat/util/net/NioBlockingSelector$BlockPoller, run, <Primordial,Z> > v1(line 320)
BB77
151   conditional branch(ne) v3,v4:#0        (line 320)
BB78
153   v110 = getfield < Application, Lorg/apache/tomcat/util/net/NioBlockingSelector$BlockPoller, events, <Application,Ljava/util/concurrent/ConcurrentLinkedQueue> > v1(line 376)
BB79
154   invokevirtual < Application, Ljava/util/concurrent/ConcurrentLinkedQueue, clear()V > v110 @325 exception:v111(line 376)
BB80
156   v112 = getfield < Application, Lorg/apache/tomcat/util/net/NioBlockingSelector$BlockPoller, selector, <Application,Ljava/nio/channels/Selector> > v1(line 378)
BB81
157   v114 = invokevirtual < Application, Ljava/nio/channels/Selector, selectNow()I > v112 @332 exception:v113(line 378)
BB82
159   goto                                   (line 378)
BB83<Handler>
           v115 = getCaughtException 
161   v117 = invokestatic < Application, Lorg/apache/tomcat/util/net/NioBlockingSelector, access$0()Lorg/apache/juli/logging/Log; > @340 exception:v116(line 380)
BB84
162   v119 = invokeinterface < Application, Lorg/apache/juli/logging/Log, isDebugEnabled()Z > v117 @343 exception:v118(line 380)
BB85
164   conditional branch(eq) v119,v4:#0      (line 380)
BB86
165   v121 = invokestatic < Application, Lorg/apache/tomcat/util/net/NioBlockingSelector, access$0()Lorg/apache/juli/logging/Log; > @351 exception:v120(line 380)
BB87
168   invokeinterface < Application, Lorg/apache/juli/logging/Log, debug(Ljava/lang/Object;Ljava/lang/Throwable;)V > v121,v100:#,v115 @357 exception:v122(line 380)
BB88
170   v125 = getfield < Application, Lorg/apache/tomcat/util/net/NioBlockingSelector$BlockPoller, selector, <Application,Ljava/nio/channels/Selector> > v1(line 383)
BB89
171   invokevirtual < Application, Ljava/nio/channels/Selector, close()V > v125 @366 exception:v126(line 383)
BB90
172   goto                                   (line 383)
BB91<Handler>
           v127 = getCaughtException 
174   v129 = invokestatic < Application, Lorg/apache/tomcat/util/net/NioBlockingSelector, access$0()Lorg/apache/juli/logging/Log; > @373 exception:v128(line 385)
BB92
175   v131 = invokeinterface < Application, Lorg/apache/juli/logging/Log, isDebugEnabled()Z > v129 @376 exception:v130(line 385)
BB93
177   conditional branch(eq) v131,v4:#0      (line 385)
BB94
178   v133 = invokestatic < Application, Lorg/apache/tomcat/util/net/NioBlockingSelector, access$0()Lorg/apache/juli/logging/Log; > @384 exception:v132(line 385)
BB95
181   invokeinterface < Application, Lorg/apache/juli/logging/Log, debug(Ljava/lang/Object;Ljava/lang/Throwable;)V > v133,v100:#,v127 @390 exception:v134(line 385)
BB96
182   return                                 (line 387)
BB97

**CGNode:** Node: < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, <clinit>()V > Context: Everywhere
**IR:** < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, <clinit>()V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..0]
    -> BB2
    -> BB22
BB2[1..1]
    -> BB3
    -> BB22
BB3[2..4]
    -> BB4
    -> BB22
BB4[5..8]
    -> BB5
    -> BB22
BB5[9..12]
    -> BB6
    -> BB22
BB6[13..16]
    -> BB7
    -> BB22
BB7[17..20]
    -> BB8
    -> BB22
BB8[21..24]
    -> BB9
    -> BB22
BB9[25..28]
    -> BB10
    -> BB22
BB10[29..32]
    -> BB11
    -> BB22
BB11[33..35]
    -> BB12
    -> BB22
BB12[36..39]
    -> BB13
    -> BB22
BB13[40..43]
    -> BB14
    -> BB22
BB14[44..47]
    -> BB15
    -> BB22
BB15[48..51]
    -> BB16
    -> BB22
BB16[52..55]
    -> BB17
    -> BB22
BB17[56..59]
    -> BB18
    -> BB22
BB18[60..63]
    -> BB19
    -> BB22
BB19[64..65]
    -> BB20
    -> BB22
BB20[66..68]
    -> BB21
    -> BB22
BB21[69..70]
    -> BB22
BB22[-1..-2]
Instructions:
BB0
BB1
0   v2 = load_metadata: <Primordial,Lorg/apache/catalina/tribes/io/XByteBuffer>, <Primordial,Ljava/lang/Class>(line 52)
BB2
1   v4 = invokestatic < Application, Lorg/apache/juli/logging/LogFactory, getLog(Ljava/lang/Class;)Lorg/apache/juli/logging/Log; > v2 @2 exception:v3(line 52)
BB3
2   putstatic v4 < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, log, <Application,Lorg/apache/juli/logging/Log> >(line 51)
4   v6 = new <Primordial,[B>@10v5:#7         (line 57)
BB4
8   arraystore v6[v7:#0] = v8:#70            (line 57)
BB5
12   arraystore v6[v9:#1] = v10:#76          (line 57)
BB6
16   arraystore v6[v11:#2] = v12:#84         (line 57)
BB7
20   arraystore v6[v13:#3] = v14:#50         (line 57)
BB8
24   arraystore v6[v15:#4] = v16:#48         (line 57)
BB9
28   arraystore v6[v17:#5] = v16:#48         (line 57)
BB10
32   arraystore v6[v18:#6] = v14:#50         (line 57)
BB11
33   putstatic v6 < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, START_DATA, <Primordial,[B> >(line 57)
35   v19 = new <Primordial,[B>@53v5:#7       (line 62)
BB12
39   arraystore v19[v7:#0] = v12:#84         (line 62)
BB13
43   arraystore v19[v9:#1] = v10:#76         (line 62)
BB14
47   arraystore v19[v11:#2] = v8:#70         (line 62)
BB15
51   arraystore v19[v13:#3] = v14:#50        (line 62)
BB16
55   arraystore v19[v15:#4] = v16:#48        (line 62)
BB17
59   arraystore v19[v17:#5] = v16:#48        (line 62)
BB18
63   arraystore v19[v18:#6] = v20:#51        (line 62)
BB19
64   putstatic v19 < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, END_DATA, <Primordial,[B> >(line 62)
65   v21 = new <Application,Ljava/util/concurrent/atomic/AtomicInteger>@94(line 557)
BB20
68   invokespecial < Application, Ljava/util/concurrent/atomic/AtomicInteger, <init>(I)V > v21,v7:#0 @99 exception:v22(line 557)
BB21
69   putstatic v21 < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, invokecount, <Application,Ljava/util/concurrent/atomic/AtomicInteger> >(line 557)
70   return                                  (line 48)
BB22

**CGNode:** Node: < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, <init>(IZ)V > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, main([Ljava/lang/String;)V >:NEW <Application,Lorg/apache/catalina/tribes/io/XByteBuffer>@19 in ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,[Ljava/lang/String>@1 in Everywhere} ]} ]
**IR:** < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, <init>(IZ)V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..1]
    -> BB2
    -> BB9
BB2[2..4]
    -> BB3
    -> BB9
BB3[5..7]
    -> BB4
    -> BB9
BB4[8..10]
    -> BB5
    -> BB9
BB5[11..13]
    -> BB6
    -> BB9
BB6[14..14]
    -> BB7
    -> BB9
BB7[15..17]
    -> BB8
    -> BB9
BB8[18..18]
    -> BB9
BB9[-1..-2]
Instructions:
BB0
BB1
1   invokespecial < Application, Ljava/lang/Object, <init>()V > v1 @1 exception:v5(line 88)
BB2
4   putfield v1 = v6:#null < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, buf, <Primordial,[B> >(line 67)
BB3
7   putfield v1 = v7:#0 < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, bufSize, <Primordial,I> >(line 72)
BB4
10   putfield v1 = v8:#1 < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, discard, <Primordial,Z> >(line 81)
BB5
13   v9 = new <Primordial,[B>@21v2           (line 89)
BB6
14   putfield v1 = v9 < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, buf, <Primordial,[B> >(line 89)
BB7
17   putfield v1 = v3 < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, discard, <Primordial,Z> >(line 90)
BB8
18   return                                  (line 91)
BB9

**CGNode:** Node: < Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive$1, <init>()V > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, main([Ljava/lang/String;)V >:NEW <Application,Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive$1>@68 in ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,[Ljava/lang/String>@1 in Everywhere} ]} ]
**IR:** < Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive$1, <init>()V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..1]
    -> BB2
    -> BB3
BB2[2..2]
    -> BB3
BB3[-1..-2]
Instructions:
BB0
BB1
1   invokespecial < Application, Ljava/lang/Thread, <init>()V > v1 @1 exception:v3(line 51)
BB2
2   return                                   (line 1)
BB3

**CGNode:** Node: < Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, printStats(JDILjava/text/DecimalFormat;Ljava/math/BigDecimal;)V > Context: ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,[Ljava/lang/String>@1 in Everywhere} ]
**IR:** < Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, printStats(JDILjava/text/DecimalFormat;Ljava/math/BigDecimal;)V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..0]
    -> BB2
    -> BB16
BB2[1..10]
    -> BB3
    -> BB16
BB3[11..13]
    -> BB4
    -> BB16
BB4[14..18]
    -> BB5
    -> BB16
BB5[19..19]
    -> BB6
    -> BB16
BB6[20..21]
    -> BB7
    -> BB16
BB7[22..23]
    -> BB8
    -> BB16
BB8[24..25]
    -> BB9
    -> BB16
BB9[26..27]
    -> BB10
    -> BB16
BB10[28..29]
    -> BB11
    -> BB16
BB11[30..31]
    -> BB12
    -> BB16
BB12[32..33]
    -> BB13
    -> BB16
BB13[34..34]
    -> BB14
    -> BB16
BB14[35..35]
    -> BB15
    -> BB16
BB15[36..36]
    -> BB16
BB16[-1..-2]
Instructions:
BB0
BB1
0   v8 = invokestatic < Application, Ljava/lang/System, currentTimeMillis()J > @0 exception:v7(line 88)
BB2
4   v9 = binaryop(sub) v8 , v1               (line 89)
5   v10 = conversion(D) v9                   (line 89)
7   v12 = binaryop(div) v10 , v11:#1000.0    (line 89)
9   v13 = getstatic < Application, Ljava/lang/System, out, <Application,Ljava/io/PrintStream> >(line 90)
10   v14 = new <Application,Ljava/lang/StringBuilder>@19(line 90)
BB3
13   invokespecial < Application, Ljava/lang/StringBuilder, <init>(Ljava/lang/String;)V > v14,v15:#Throughput  @25 exception:v16(line 90)
BB4
17   v17 = binaryop(div) v2 , v12            (line 90)
18   v19 = invokevirtual < Application, Ljava/text/DecimalFormat, format(D)Ljava/lang/String; > v4,v17 @34 exception:v18(line 90)
BB5
19   v21 = invokevirtual < Application, Ljava/lang/StringBuilder, append(Ljava/lang/String;)Ljava/lang/StringBuilder; > v14,v19 @37 exception:v20(line 90)
BB6
21   v24 = invokevirtual < Application, Ljava/lang/StringBuilder, append(Ljava/lang/String;)Ljava/lang/StringBuilder; > v21,v22:# MB/seconds messages  @42 exception:v23(line 90)
BB7
23   v26 = invokevirtual < Application, Ljava/lang/StringBuilder, append(I)Ljava/lang/StringBuilder; > v24,v3 @47 exception:v25(line 90)
BB8
25   v29 = invokevirtual < Application, Ljava/lang/StringBuilder, append(Ljava/lang/String;)Ljava/lang/StringBuilder; > v26,v27:#, total  @52 exception:v28(line 90)
BB9
27   v31 = invokevirtual < Application, Ljava/lang/StringBuilder, append(D)Ljava/lang/StringBuilder; > v29,v2 @56 exception:v30(line 90)
BB10
29   v34 = invokevirtual < Application, Ljava/lang/StringBuilder, append(Ljava/lang/String;)Ljava/lang/StringBuilder; > v31,v32:# MB, total  @61 exception:v33(line 90)
BB11
31   v36 = invokevirtual < Application, Ljava/lang/StringBuilder, append(Ljava/lang/Object;)Ljava/lang/StringBuilder; > v34,v5 @66 exception:v35(line 90)
BB12
33   v39 = invokevirtual < Application, Ljava/lang/StringBuilder, append(Ljava/lang/String;)Ljava/lang/StringBuilder; > v36,v37:# bytes. @71 exception:v38(line 90)
BB13
34   v41 = invokevirtual < Application, Ljava/lang/StringBuilder, toString()Ljava/lang/String; > v39 @74 exception:v40(line 90)
BB14
35   invokevirtual < Application, Ljava/io/PrintStream, println(Ljava/lang/String;)V > v13,v41 @77 exception:v42(line 90)
BB15
36   return                                  (line 91)
BB16

**CGNode:** Node: < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, append([BII)Z > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, main([Ljava/lang/String;)V >:NEW <Application,Lorg/apache/catalina/tribes/io/XByteBuffer>@19 in ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,[Ljava/lang/String>@1 in Everywhere} ]} ]
**IR:** < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, append([BII)Z >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..2]
    -> BB8
    -> BB2
BB2[3..5]
    -> BB3
    -> BB34
BB3[6..6]
    -> BB8
    -> BB4
BB4[7..9]
    -> BB8
    -> BB5
BB5[10..14]
    -> BB6
    -> BB34
BB6[15..15]
    -> BB8
    -> BB7
BB7[16..20]
    -> BB11
    -> BB8
BB8[21..21]
    -> BB9
    -> BB34
BB9[22..23]
    -> BB10
    -> BB34
BB10[24..24]
    -> BB34
BB11[25..27]
    -> BB13
    -> BB12
BB12[28..29]
    -> BB34
BB13[30..31]
    -> BB14
    -> BB34
BB14[32..37]
    -> BB15
    -> BB34
BB15[38..38]
    -> BB16
    -> BB34
BB16[39..39]
    -> BB18
    -> BB17
BB17[40..42]
    -> BB18
    -> BB34
BB18[43..46]
    -> BB19
    -> BB34
BB19[47..48]
    -> BB20
    -> BB34
BB20[49..50]
    -> BB21
    -> BB34
BB21[51..53]
    -> BB22
    -> BB34
BB22[54..55]
    -> BB23
    -> BB34
BB23[56..57]
    -> BB33
    -> BB24
BB24[58..59]
    -> BB25
    -> BB34
BB25[60..61]
    -> BB26
    -> BB34
BB26[62..62]
    -> BB33
    -> BB27
BB27[63..64]
    -> BB28
    -> BB34
BB28[65..67]
    -> BB29
    -> BB34
BB29[68..69]
    -> BB33
    -> BB30
BB30[70..72]
    -> BB31
    -> BB34
BB31[73..75]
    -> BB32
    -> BB34
BB32[76..77]
    -> BB34
BB33[78..79]
    -> BB34
BB34[-1..-2]
Instructions:
BB0
BB1
2   conditional branch(lt) v3,v6:#0          (line 213)
BB2
5   v7 = arraylength v2                      (line 213)
BB3
6   conditional branch(gt) v3,v7             (line 213)
BB4
9   conditional branch(lt) v4,v6:#0          (line 213)
BB5
12   v8 = binaryop(add) v3 , v4              (line 214)
14   v9 = arraylength v2                     (line 214)
BB6
15   conditional branch(gt) v8,v9            (line 214)
BB7
18   v10 = binaryop(add) v3 , v4             (line 214)
20   conditional branch(ge) v10,v6:#0        (line 214)
BB8
21   v32 = new <Application,Ljava/lang/IndexOutOfBoundsException>@28(line 215)
BB9
23   invokespecial < Application, Ljava/lang/IndexOutOfBoundsException, <init>()V > v32 @32 exception:v33(line 215)
BB10
24   throw v32                               (line 215)
BB11
27   conditional branch(ne) v4,v6:#0         (line 216)
BB12
29   return v6:#0                            (line 217)
BB13
31   v11 = getfield < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, bufSize, <Primordial,I> > v1(line 220)
BB14
33   v12 = binaryop(add) v11 , v4            (line 220)
37   v13 = getfield < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, buf, <Primordial,[B> > v1(line 221)
BB15
38   v14 = arraylength v13                   (line 221)
BB16
39   conditional branch(le) v12,v14          (line 221)
BB17
42   invokevirtual < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, expand(I)V > v1,v12 @63 exception:v15(line 222)
BB18
46   v16 = getfield < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, buf, <Primordial,[B> > v1(line 224)
BB19
48   v17 = getfield < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, bufSize, <Primordial,I> > v1(line 224)
BB20
50   invokestatic < Application, Ljava/lang/System, arraycopy(Ljava/lang/Object;ILjava/lang/Object;II)V > v2,v3,v16,v17,v4 @77 exception:v18(line 224)
BB21
53   putfield v1 = v12 < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, bufSize, <Primordial,I> >(line 225)
BB22
55   v19 = getfield < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, discard, <Primordial,Z> > v1(line 227)
BB23
57   conditional branch(eq) v19,v6:#0        (line 227)
BB24
59   v20 = getfield < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, bufSize, <Primordial,I> > v1(line 228)
BB25
60   v21 = getstatic < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, START_DATA, <Primordial,[B> >(line 228)
61   v22 = arraylength v21                   (line 228)
BB26
62   conditional branch(le) v20,v22          (line 228)
BB27
64   v23 = getfield < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, buf, <Primordial,[B> > v1(line 228)
BB28
66   v24 = getstatic < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, START_DATA, <Primordial,[B> >(line 228)
67   v26 = invokestatic < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, firstIndexOf([BI[B)I > v23,v6:#0,v24 @112 exception:v25(line 228)
BB29
69   conditional branch(ne) v26,v27:#-1      (line 228)
BB30
72   putfield v1 = v6:#0 < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, bufSize, <Primordial,I> >(line 229)
BB31
73   v29 = getstatic < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, log, <Application,Lorg/apache/juli/logging/Log> >(line 230)
75   invokeinterface < Application, Lorg/apache/juli/logging/Log, error(Ljava/lang/Object;)V > v29,v30:#Discarded the package, invalid header @129 exception:v31(line 230)
BB32
77   return v6:#0                            (line 231)
BB33
79   return v28:#1                           (line 234)
BB34

**CGNode:** Node: < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, extractPackage(Z)Lorg/apache/catalina/tribes/io/ChannelData; > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, main([Ljava/lang/String;)V >:NEW <Application,Lorg/apache/catalina/tribes/io/XByteBuffer>@19 in ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,[Ljava/lang/String>@1 in Everywhere} ]} ]
**IR:** < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, extractPackage(Z)Lorg/apache/catalina/tribes/io/ChannelData; >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..2]
    -> BB2
    -> BB4
BB2[3..5]
    -> BB3
    -> BB4
BB3[6..8]
    -> BB4
BB4[-1..-2]
Instructions:
BB0
BB1
2   v5 = invokevirtual < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, extractDataPackage(Z)Lorg/apache/catalina/tribes/io/XByteBuffer; > v1,v2 @2 exception:v4(line 325)
BB2
5   v7 = invokestatic < Application, Lorg/apache/catalina/tribes/io/ChannelData, getDataFromPackage(Lorg/apache/catalina/tribes/io/XByteBuffer;)Lorg/apache/catalina/tribes/io/ChannelData; > v5 @7 exception:v6(line 326)
BB3
8   return v7                                (line 327)
BB4

**CGNode:** Node: < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, countPackages(Z)I > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, main([Ljava/lang/String;)V >:NEW <Application,Lorg/apache/catalina/tribes/io/XByteBuffer>@19 in ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,[Ljava/lang/String>@1 in Everywhere} ]} ]
**IR:** < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, countPackages(Z)I >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..3]
    -> BB2
    -> BB27
BB2[4..7]
    -> BB24
BB3[8..9]
    -> BB4
    -> BB27
BB4[10..12]
    -> BB5
    -> BB27
BB5[13..16]
    -> BB26
    -> BB6
BB6[17..18]
    -> BB7
    -> BB27
BB7[19..22]
    -> BB9
    -> BB8
BB8[23..23]
    -> BB26
BB9[24..25]
    -> BB10
    -> BB27
BB10[26..27]
    -> BB11
    -> BB27
BB11[28..31]
    -> BB12
    -> BB27
BB12[32..40]
    -> BB13
    -> BB27
BB13[41..43]
    -> BB14
    -> BB27
BB14[44..44]
    -> BB16
    -> BB15
BB15[45..45]
    -> BB26
BB16[46..47]
    -> BB17
    -> BB27
BB17[48..50]
    -> BB18
    -> BB27
BB18[51..54]
    -> BB20
    -> BB19
BB19[55..55]
    -> BB26
BB20[56..62]
    -> BB21
    -> BB27
BB21[63..67]
    -> BB22
    -> BB27
BB22[68..72]
    -> BB24
    -> BB23
BB23[73..73]
    -> BB26
BB24[74..76]
    -> BB25
    -> BB27
BB25[77..77]
    -> BB3
    -> BB26
BB26[78..79]
    -> BB27
BB27[-1..-2]
Instructions:
BB0
BB1
2   v5 = getstatic < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, START_DATA, <Primordial,[B> >(line 261)
3   v6 = arraylength v5                      (line 261)
BB2
7   goto                                     (line 264)
BB3
9   v8 = getfield < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, buf, <Primordial,[B> > v1(line 266)
BB4
11   v9 = getstatic < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, START_DATA, <Primordial,[B> >(line 266)
12   v11 = invokestatic < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, firstIndexOf([BI[B)I > v8,v42,v9 @22 exception:v10(line 266)
BB5
16   conditional branch(ne) v11,v42          (line 269)
BB6
18   v12 = getfield < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, bufSize, <Primordial,I> > v1(line 269)
BB7
20   v13 = binaryop(sub) v12 , v42           (line 269)
22   conditional branch(ge) v13,v14:#14      (line 269)
BB8
23   goto                                    (line 269)
BB9
25   v15 = getfield < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, buf, <Primordial,[B> > v1(line 272)
BB10
27   v17 = invokestatic < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, toInt([BI)I > v15,v41 @54 exception:v16(line 272)
BB11
30   v18 = getstatic < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, START_DATA, <Primordial,[B> >(line 275)
31   v19 = arraylength v18                   (line 275)
BB12
32   v20 = binaryop(add) v42 , v19           (line 275)
34   v22 = binaryop(add) v20 , v21:#4        (line 275)
36   v23 = binaryop(add) v22 , v17           (line 275)
39   v24 = getstatic < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, END_DATA, <Primordial,[B> >(line 276)
40   v25 = arraylength v24                   (line 276)
BB13
41   v26 = binaryop(add) v23 , v25           (line 276)
43   v27 = getfield < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, bufSize, <Primordial,I> > v1(line 276)
BB14
44   conditional branch(le) v26,v27          (line 276)
BB15
45   goto                                    (line 276)
BB16
47   v28 = getfield < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, buf, <Primordial,[B> > v1(line 278)
BB17
49   v29 = getstatic < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, END_DATA, <Primordial,[B> >(line 278)
50   v31 = invokestatic < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, firstIndexOf([BI[B)I > v28,v23,v29 @96 exception:v30(line 278)
BB18
54   conditional branch(eq) v31,v23          (line 280)
BB19
55   goto                                    (line 280)
BB20
58   v33 = binaryop(add) v40 , v32:#1        (line 282)
61   v34 = getstatic < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, END_DATA, <Primordial,[B> >(line 284)
62   v35 = arraylength v34                   (line 284)
BB21
63   v36 = binaryop(add) v23 , v35           (line 284)
66   v37 = getstatic < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, START_DATA, <Primordial,[B> >(line 285)
67   v38 = arraylength v37                   (line 285)
BB22
68   v39 = binaryop(add) v36 , v38           (line 285)
72   conditional branch(eq) v2,v4:#0         (line 287)
BB23
73   goto                                    (line 287)
BB24
           v40 = phi  v4:#0,v33
           v41 = phi  v6,v39
           v42 = phi  v4:#0,v36
76   v7 = getfield < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, bufSize, <Primordial,I> > v1(line 264)
BB25
77   conditional branch(lt) v42,v7           (line 264)
BB26
           v43 = phi  v40,v40,v40,v40,v33,v40
79   return v43                              (line 289)
BB27

**CGNode:** Node: < Application, Lorg/apache/tomcat/util/net/AprEndpoint, <clinit>()V > Context: Everywhere
**IR:** < Application, Lorg/apache/tomcat/util/net/AprEndpoint, <clinit>()V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..0]
    -> BB2
    -> BB4
BB2[1..1]
    -> BB3
    -> BB4
BB3[2..3]
    -> BB4
BB4[-1..-2]
Instructions:
BB0
BB1
0   v2 = load_metadata: <Primordial,Lorg/apache/tomcat/util/net/AprEndpoint>, <Primordial,Ljava/lang/Class>(line 69)
BB2
1   v4 = invokestatic < Application, Lorg/apache/juli/logging/LogFactory, getLog(Ljava/lang/Class;)Lorg/apache/juli/logging/Log; > v2 @2 exception:v3(line 69)
BB3
2   putstatic v4 < Application, Lorg/apache/tomcat/util/net/AprEndpoint, log, <Application,Lorg/apache/juli/logging/Log> >(line 69)
3   return                                   (line 63)
BB4

**CGNode:** Node: < Application, Lorg/apache/tomcat/util/net/AprEndpoint, <init>()V > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, main([Ljava/lang/String;)V >:NEW <Application,Lorg/apache/tomcat/util/net/AprEndpoint>@0 in ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,[Ljava/lang/String>@6 in Everywhere} ]} ]
**IR:** < Application, Lorg/apache/tomcat/util/net/AprEndpoint, <init>()V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..1]
    -> BB2
    -> BB38
BB2[2..4]
    -> BB3
    -> BB38
BB3[5..7]
    -> BB4
    -> BB38
BB4[8..10]
    -> BB5
    -> BB38
BB5[11..13]
    -> BB6
    -> BB38
BB6[14..15]
    -> BB7
    -> BB38
BB7[16..17]
    -> BB8
    -> BB38
BB8[18..18]
    -> BB9
    -> BB38
BB9[19..21]
    -> BB10
    -> BB38
BB10[22..24]
    -> BB11
    -> BB38
BB11[25..27]
    -> BB12
    -> BB38
BB12[28..30]
    -> BB13
    -> BB38
BB13[31..33]
    -> BB14
    -> BB38
BB14[34..36]
    -> BB15
    -> BB38
BB15[37..39]
    -> BB16
    -> BB38
BB16[40..42]
    -> BB17
    -> BB38
BB17[43..45]
    -> BB18
    -> BB38
BB18[46..48]
    -> BB19
    -> BB38
BB19[49..51]
    -> BB20
    -> BB38
BB20[52..54]
    -> BB21
    -> BB38
BB21[55..57]
    -> BB22
    -> BB38
BB22[58..60]
    -> BB23
    -> BB38
BB23[61..63]
    -> BB24
    -> BB38
BB24[64..66]
    -> BB25
    -> BB38
BB25[67..69]
    -> BB26
    -> BB38
BB26[70..72]
    -> BB27
    -> BB38
BB27[73..75]
    -> BB28
    -> BB38
BB28[76..78]
    -> BB29
    -> BB38
BB29[79..81]
    -> BB30
    -> BB38
BB30[82..84]
    -> BB31
    -> BB38
BB31[85..87]
    -> BB32
    -> BB38
BB32[88..90]
    -> BB33
    -> BB38
BB33[91..93]
    -> BB34
    -> BB38
BB34[94..96]
    -> BB35
    -> BB38
BB35[97..99]
    -> BB36
    -> BB38
BB36[100..102]
    -> BB37
    -> BB38
BB37[103..103]
    -> BB38
BB38[-1..-2]
Instructions:
BB0
BB1
1   invokespecial < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, <init>()V > v1 @1 exception:v3(line 101)
BB2
4   putfield v1 = v4:#0 < Application, Lorg/apache/tomcat/util/net/AprEndpoint, rootPool, <Primordial,J> >(line 75)
BB3
7   putfield v1 = v4:#0 < Application, Lorg/apache/tomcat/util/net/AprEndpoint, serverSock, <Primordial,J> >(line 81)
BB4
10   putfield v1 = v4:#0 < Application, Lorg/apache/tomcat/util/net/AprEndpoint, serverSockPool, <Primordial,J> >(line 87)
BB5
13   putfield v1 = v4:#0 < Application, Lorg/apache/tomcat/util/net/AprEndpoint, sslContext, <Primordial,J> >(line 93)
BB6
15   v5 = new <Application,Ljava/util/concurrent/ConcurrentLinkedQueue>@25(line 97)
BB7
17   invokespecial < Application, Ljava/util/concurrent/ConcurrentLinkedQueue, <init>()V > v5 @29 exception:v6(line 97)
BB8
18   putfield v1 = v5 < Application, Lorg/apache/tomcat/util/net/AprEndpoint, waitingRequests, <Application,Ljava/util/concurrent/ConcurrentLinkedQueue> >(line 97)
BB9
21   putfield v1 = v7:#1 < Application, Lorg/apache/tomcat/util/net/AprEndpoint, deferAccept, <Primordial,Z> >(line 113)
BB10
24   putfield v1 = v8:#1024 < Application, Lorg/apache/tomcat/util/net/AprEndpoint, sendfileSize, <Primordial,I> >(line 122)
BB11
27   putfield v1 = v9:#null < Application, Lorg/apache/tomcat/util/net/AprEndpoint, handler, <Application,Lorg/apache/tomcat/util/net/AprEndpoint$Handler> >(line 130)
BB12
30   putfield v1 = v10:#2000 < Application, Lorg/apache/tomcat/util/net/AprEndpoint, pollTime, <Primordial,I> >(line 139)
BB13
32   v11 = getstatic < Application, Lorg/apache/tomcat/jni/Library, APR_HAS_SENDFILE, <Primordial,Z> >(line 147)
33   putfield v1 = v11 < Application, Lorg/apache/tomcat/util/net/AprEndpoint, useSendfile, <Primordial,Z> >(line 147)
BB14
36   putfield v1 = v7:#1 < Application, Lorg/apache/tomcat/util/net/AprEndpoint, useComet, <Primordial,Z> >(line 156)
BB15
39   putfield v1 = v12:#0 < Application, Lorg/apache/tomcat/util/net/AprEndpoint, sendfileThreadCount, <Primordial,I> >(line 169)
BB16
42   putfield v1 = v12:#0 < Application, Lorg/apache/tomcat/util/net/AprEndpoint, pollerThreadCount, <Primordial,I> >(line 177)
BB17
45   putfield v1 = v9:#null < Application, Lorg/apache/tomcat/util/net/AprEndpoint, pollers, <Application,[Lorg/apache/tomcat/util/net/AprEndpoint$Poller> >(line 185)
BB18
48   putfield v1 = v12:#0 < Application, Lorg/apache/tomcat/util/net/AprEndpoint, pollerRoundRobin, <Primordial,I> >(line 186)
BB19
51   putfield v1 = v9:#null < Application, Lorg/apache/tomcat/util/net/AprEndpoint, cometPollers, <Application,[Lorg/apache/tomcat/util/net/AprEndpoint$Poller> >(line 196)
BB20
54   putfield v1 = v12:#0 < Application, Lorg/apache/tomcat/util/net/AprEndpoint, cometPollerRoundRobin, <Primordial,I> >(line 197)
BB21
57   putfield v1 = v9:#null < Application, Lorg/apache/tomcat/util/net/AprEndpoint, sendfiles, <Application,[Lorg/apache/tomcat/util/net/AprEndpoint$Sendfile> >(line 207)
BB22
60   putfield v1 = v12:#0 < Application, Lorg/apache/tomcat/util/net/AprEndpoint, sendfileRoundRobin, <Primordial,I> >(line 208)
BB23
63   putfield v1 = v13:#all < Application, Lorg/apache/tomcat/util/net/AprEndpoint, SSLProtocol, <Application,Ljava/lang/String> >(line 218)
BB24
66   putfield v1 = v9:#null < Application, Lorg/apache/tomcat/util/net/AprEndpoint, SSLPassword, <Application,Ljava/lang/String> >(line 227)
BB25
69   putfield v1 = v14:#ALL < Application, Lorg/apache/tomcat/util/net/AprEndpoint, SSLCipherSuite, <Application,Ljava/lang/String> >(line 235)
BB26
72   putfield v1 = v9:#null < Application, Lorg/apache/tomcat/util/net/AprEndpoint, SSLCertificateFile, <Application,Ljava/lang/String> >(line 243)
BB27
75   putfield v1 = v9:#null < Application, Lorg/apache/tomcat/util/net/AprEndpoint, SSLCertificateKeyFile, <Application,Ljava/lang/String> >(line 251)
BB28
78   putfield v1 = v9:#null < Application, Lorg/apache/tomcat/util/net/AprEndpoint, SSLCertificateChainFile, <Application,Ljava/lang/String> >(line 259)
BB29
81   putfield v1 = v9:#null < Application, Lorg/apache/tomcat/util/net/AprEndpoint, SSLCACertificatePath, <Application,Ljava/lang/String> >(line 267)
BB30
84   putfield v1 = v9:#null < Application, Lorg/apache/tomcat/util/net/AprEndpoint, SSLCACertificateFile, <Application,Ljava/lang/String> >(line 275)
BB31
87   putfield v1 = v9:#null < Application, Lorg/apache/tomcat/util/net/AprEndpoint, SSLCARevocationPath, <Application,Ljava/lang/String> >(line 283)
BB32
90   putfield v1 = v9:#null < Application, Lorg/apache/tomcat/util/net/AprEndpoint, SSLCARevocationFile, <Application,Ljava/lang/String> >(line 291)
BB33
93   putfield v1 = v15:#none < Application, Lorg/apache/tomcat/util/net/AprEndpoint, SSLVerifyClient, <Application,Ljava/lang/String> >(line 299)
BB34
96   putfield v1 = v16:#10 < Application, Lorg/apache/tomcat/util/net/AprEndpoint, SSLVerifyDepth, <Primordial,I> >(line 307)
BB35
99   putfield v1 = v12:#0 < Application, Lorg/apache/tomcat/util/net/AprEndpoint, SSLInsecureRenegotiation, <Primordial,Z> >(line 316)
BB36
102   invokevirtual < Application, Lorg/apache/tomcat/util/net/AprEndpoint, setMaxConnections(I)V > v1,v17:#8192 @184 exception:v18(line 104)
BB37
103   return                                 (line 105)
BB38

**CGNode:** Node: < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, startAcceptorThreads()V > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, main([Ljava/lang/String;)V >:NEW <Application,Lorg/apache/tomcat/util/net/AprEndpoint>@0 in ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,[Ljava/lang/String>@6 in Everywhere} ]} ]
**IR:** < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, startAcceptorThreads()V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..1]
    -> BB2
    -> BB27
BB2[2..5]
    -> BB3
    -> BB27
BB3[6..6]
    -> BB4
    -> BB27
BB4[7..9]
    -> BB25
BB5[10..11]
    -> BB6
    -> BB27
BB6[12..14]
    -> BB7
    -> BB27
BB7[15..15]
    -> BB8
    -> BB27
BB8[16..16]
    -> BB9
    -> BB27
BB9[17..19]
    -> BB10
    -> BB27
BB10[20..21]
    -> BB11
    -> BB27
BB11[22..22]
    -> BB12
    -> BB27
BB12[23..25]
    -> BB13
    -> BB27
BB13[26..26]
    -> BB14
    -> BB27
BB14[27..27]
    -> BB15
    -> BB27
BB15[28..29]
    -> BB16
    -> BB27
BB16[30..31]
    -> BB17
    -> BB27
BB17[32..32]
    -> BB18
    -> BB27
BB18[33..33]
    -> BB19
    -> BB27
BB19[34..37]
    -> BB20
    -> BB27
BB20[38..38]
    -> BB21
    -> BB27
BB21[39..41]
    -> BB22
    -> BB27
BB22[42..42]
    -> BB23
    -> BB27
BB23[43..44]
    -> BB24
    -> BB27
BB24[45..48]
    -> BB25
BB25[49..51]
    -> BB5
    -> BB26
BB26[52..52]
    -> BB27
BB27[-1..-2]
Instructions:
BB0
BB1
1   v4 = invokevirtual < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, getAcceptorThreadCount()I > v1 @1 exception:v3(line 587)
BB2
5   v5 = new <Application,[Lorg/apache/tomcat/util/net/AbstractEndpoint$Acceptor>@7v4 (line 588)
BB3
6   putfield v1 = v5 < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, acceptors, <Application,[Lorg/apache/tomcat/util/net/AbstractEndpoint$Acceptor> >(line 588)
BB4
9   goto                                     (line 590)
BB5
11   v7 = getfield < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, acceptors, <Application,[Lorg/apache/tomcat/util/net/AbstractEndpoint$Acceptor> > v1(line 591)
BB6
14   v9 = invokevirtual < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, createAcceptor()Lorg/apache/tomcat/util/net/AbstractEndpoint$Acceptor; > v1 @24 exception:v8(line 591)
BB7
15   arraystore v7[v36] = v9                 (line 591)
BB8
16   v10 = new <Application,Ljava/lang/Thread>@28(line 592)
BB9
19   v11 = getfield < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, acceptors, <Application,[Lorg/apache/tomcat/util/net/AbstractEndpoint$Acceptor> > v1(line 592)
BB10
21   v12 = arrayload v11[v36]                (line 592)
BB11
22   v13 = new <Application,Ljava/lang/StringBuilder>@38(line 592)
BB12
25   v15 = invokevirtual < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, getName()Ljava/lang/String; > v1 @43 exception:v14(line 592)
BB13
26   v17 = invokestatic < Application, Ljava/lang/String, valueOf(Ljava/lang/Object;)Ljava/lang/String; > v15 @46 exception:v16(line 592)
BB14
27   invokespecial < Application, Ljava/lang/StringBuilder, <init>(Ljava/lang/String;)V > v13,v17 @49 exception:v18(line 592)
BB15
29   v21 = invokevirtual < Application, Ljava/lang/StringBuilder, append(Ljava/lang/String;)Ljava/lang/StringBuilder; > v13,v19:#-Acceptor- @55 exception:v20(line 592)
BB16
31   v23 = invokevirtual < Application, Ljava/lang/StringBuilder, append(I)Ljava/lang/StringBuilder; > v21,v36 @59 exception:v22(line 592)
BB17
32   v25 = invokevirtual < Application, Ljava/lang/StringBuilder, toString()Ljava/lang/String; > v23 @62 exception:v24(line 592)
BB18
33   invokespecial < Application, Ljava/lang/Thread, <init>(Ljava/lang/Runnable;Ljava/lang/String;)V > v10,v12,v25 @65 exception:v26(line 592)
BB19
37   v28 = invokevirtual < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, getAcceptorThreadPriority()I > v1 @71 exception:v27(line 593)
BB20
38   invokevirtual < Application, Ljava/lang/Thread, setPriority(I)V > v10,v28 @74 exception:v29(line 593)
BB21
41   v31 = invokevirtual < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, getDaemon()Z > v1 @79 exception:v30(line 594)
BB22
42   invokevirtual < Application, Ljava/lang/Thread, setDaemon(Z)V > v10,v31 @82 exception:v32(line 594)
BB23
44   invokevirtual < Application, Ljava/lang/Thread, start()V > v10 @86 exception:v33(line 595)
BB24
47   v35 = binaryop(add) v36 , v34:#1        (line 590)
BB25
           v36 = phi  v6:#0,v35
51   conditional branch(lt) v36,v4           (line 590)
BB26
52   return                                  (line 597)
BB27

**CGNode:** Node: < Application, Lorg/apache/tomcat/util/res/StringManager, getManager(Ljava/lang/String;)Lorg/apache/tomcat/util/res/StringManager; > Context: ReceiverStringContext: [ [<Primordial,Ljava/lang/String>] ]
**IR:** < Application, Lorg/apache/tomcat/util/res/StringManager, getManager(Ljava/lang/String;)Lorg/apache/tomcat/util/res/StringManager; >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..1]
    -> BB2
    -> BB4
BB2[2..2]
    -> BB3
    -> BB4
BB3[3..3]
    -> BB4
BB4[-1..-2]
Instructions:
BB0
BB1
1   v4 = invokestatic < Application, Ljava/util/Locale, getDefault()Ljava/util/Locale; > @1 exception:v3(line 179)
BB2
2   v6 = invokestatic < Application, Lorg/apache/tomcat/util/res/StringManager, getManager(Ljava/lang/String;Ljava/util/Locale;)Lorg/apache/tomcat/util/res/StringManager; > v1,v4 @4 exception:v5(line 179)
BB3
3   return v6                                (line 179)
BB4

**CGNode:** Node: < Application, Lorg/apache/tomcat/util/res/StringManager, <clinit>()V > Context: Everywhere
**IR:** < Application, Lorg/apache/tomcat/util/res/StringManager, <clinit>()V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..0]
    -> BB2
    -> BB4
BB2[1..2]
    -> BB3
    -> BB4
BB3[3..4]
    -> BB4
BB4[-1..-2]
Instructions:
BB0
BB1
0   v2 = new <Application,Ljava/util/Hashtable>@0(line 168)
BB2
2   invokespecial < Application, Ljava/util/Hashtable, <init>()V > v2 @4 exception:v3(line 168)
BB3
3   putstatic v2 < Application, Lorg/apache/tomcat/util/res/StringManager, managers, <Application,Ljava/util/Map> >(line 167)
4   return                                   (line 54)
BB4

**CGNode:** Node: < Application, Lorg/apache/juli/logging/LogFactory, getLog(Ljava/lang/Class;)Lorg/apache/juli/logging/Log; > Context: ReceiverStringContext: [ [<Primordial,Ljava/lang/Class>] ]
**IR:** < Application, Lorg/apache/juli/logging/LogFactory, getLog(Ljava/lang/Class;)Lorg/apache/juli/logging/Log; >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..0]
    -> BB2
    -> BB4
BB2[1..2]
    -> BB3
    -> BB4
BB3[3..3]
    -> BB4
BB4[-1..-2]
Instructions:
BB0
BB1
0   v4 = invokestatic < Application, Lorg/apache/juli/logging/LogFactory, getFactory()Lorg/apache/juli/logging/LogFactory; > @0 exception:v3(line 165)
BB2
2   v6 = invokevirtual < Application, Lorg/apache/juli/logging/LogFactory, getInstance(Ljava/lang/Class;)Lorg/apache/juli/logging/Log; > v4,v1 @4 exception:v5(line 165)
BB3
3   return v6                                (line 165)
BB4

**CGNode:** Node: < Application, Lorg/apache/juli/logging/LogFactory, <clinit>()V > Context: Everywhere
**IR:** < Application, Lorg/apache/juli/logging/LogFactory, <clinit>()V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..0]
    -> BB2
    -> BB4
BB2[1..2]
    -> BB3
    -> BB4
BB3[3..4]
    -> BB4
BB4[-1..-2]
Instructions:
BB0
BB1
0   v2 = new <Application,Lorg/apache/juli/logging/LogFactory>@0(line 66)
BB2
2   invokespecial < Application, Lorg/apache/juli/logging/LogFactory, <init>()V > v2 @4 exception:v3(line 66)
BB3
3   putstatic v2 < Application, Lorg/apache/juli/logging/LogFactory, singleton, <Application,Lorg/apache/juli/logging/LogFactory> >(line 66)
4   return                                   (line 64)
BB4

**CGNode:** Node: < Application, Lorg/apache/catalina/tribes/group/ChannelInterceptorBase, <init>()V > Context: ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,Lorg/apache/catalina/tribes/group/interceptors/MessageDispatchInterceptor>@11 in Everywhere} ]
**IR:** < Application, Lorg/apache/catalina/tribes/group/ChannelInterceptorBase, <init>()V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..1]
    -> BB2
    -> BB4
BB2[2..4]
    -> BB3
    -> BB4
BB3[5..5]
    -> BB4
BB4[-1..-2]
Instructions:
BB0
BB1
1   invokespecial < Application, Ljava/lang/Object, <init>()V > v1 @1 exception:v3(line 37)
BB2
4   putfield v1 = v4:#0 < Application, Lorg/apache/catalina/tribes/group/ChannelInterceptorBase, optionFlag, <Primordial,I> >(line 35)
BB3
5   return                                   (line 39)
BB4

**CGNode:** Node: < Application, Lorg/apache/catalina/tribes/transport/bio/util/FastQueue, <clinit>()V > Context: Everywhere
**IR:** < Application, Lorg/apache/catalina/tribes/transport/bio/util/FastQueue, <clinit>()V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..0]
    -> BB2
    -> BB4
BB2[1..1]
    -> BB3
    -> BB4
BB3[2..3]
    -> BB4
BB4[-1..-2]
Instructions:
BB0
BB1
0   v2 = load_metadata: <Primordial,Lorg/apache/catalina/tribes/transport/bio/util/FastQueue>, <Primordial,Ljava/lang/Class>(line 37)
BB2
1   v4 = invokestatic < Application, Lorg/apache/juli/logging/LogFactory, getLog(Ljava/lang/Class;)Lorg/apache/juli/logging/Log; > v2 @2 exception:v3(line 37)
BB3
2   putstatic v4 < Application, Lorg/apache/catalina/tribes/transport/bio/util/FastQueue, log, <Application,Lorg/apache/juli/logging/Log> >(line 37)
3   return                                   (line 35)
BB4

**CGNode:** Node: < Application, Lorg/apache/catalina/tribes/transport/bio/util/FastQueue, <init>()V > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/group/interceptors/MessageDispatchInterceptor, <init>()V >:NEW <Application,Lorg/apache/catalina/tribes/transport/bio/util/FastQueue>@12 in ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,Lorg/apache/catalina/tribes/group/interceptors/MessageDispatchInterceptor>@11 in Everywhere} ]} ]
**IR:** < Application, Lorg/apache/catalina/tribes/transport/bio/util/FastQueue, <init>()V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..1]
    -> BB2
    -> BB20
BB2[2..4]
    -> BB3
    -> BB20
BB3[5..7]
    -> BB4
    -> BB20
BB4[8..10]
    -> BB5
    -> BB20
BB5[11..13]
    -> BB6
    -> BB20
BB6[14..16]
    -> BB7
    -> BB20
BB7[17..19]
    -> BB8
    -> BB20
BB8[20..22]
    -> BB9
    -> BB20
BB9[23..25]
    -> BB10
    -> BB20
BB10[26..27]
    -> BB11
    -> BB20
BB11[28..29]
    -> BB12
    -> BB20
BB12[30..30]
    -> BB13
    -> BB20
BB13[31..32]
    -> BB14
    -> BB20
BB14[33..34]
    -> BB15
    -> BB20
BB15[35..35]
    -> BB16
    -> BB20
BB16[36..37]
    -> BB17
    -> BB20
BB17[38..39]
    -> BB18
    -> BB20
BB18[40..40]
    -> BB19
    -> BB20
BB19[41..41]
    -> BB20
BB20[-1..-2]
Instructions:
BB0
BB1
1   invokespecial < Application, Ljava/lang/Object, <init>()V > v1 @1 exception:v3(line 89)
BB2
4   putfield v1 = v4:#null < Application, Lorg/apache/catalina/tribes/transport/bio/util/FastQueue, first, <Application,Lorg/apache/catalina/tribes/transport/bio/util/LinkObject> >(line 47)
BB3
7   putfield v1 = v4:#null < Application, Lorg/apache/catalina/tribes/transport/bio/util/FastQueue, last, <Application,Lorg/apache/catalina/tribes/transport/bio/util/LinkObject> >(line 52)
BB4
10   putfield v1 = v5:#0 < Application, Lorg/apache/catalina/tribes/transport/bio/util/FastQueue, size, <Primordial,I> >(line 57)
BB5
13   putfield v1 = v5:#0 < Application, Lorg/apache/catalina/tribes/transport/bio/util/FastQueue, maxQueueLength, <Primordial,I> >(line 62)
BB6
16   putfield v1 = v6:#10000 < Application, Lorg/apache/catalina/tribes/transport/bio/util/FastQueue, addWaitTimeout, <Primordial,J> >(line 67)
BB7
19   putfield v1 = v7:#30000 < Application, Lorg/apache/catalina/tribes/transport/bio/util/FastQueue, removeWaitTimeout, <Primordial,J> >(line 73)
BB8
22   putfield v1 = v8:#1 < Application, Lorg/apache/catalina/tribes/transport/bio/util/FastQueue, enabled, <Primordial,Z> >(line 78)
BB9
25   putfield v1 = v5:#0 < Application, Lorg/apache/catalina/tribes/transport/bio/util/FastQueue, maxSize, <Primordial,I> >(line 83)
BB10
27   v9 = new <Application,Lorg/apache/catalina/tribes/transport/bio/util/SingleRemoveSynchronizedAddLock>@49(line 90)
BB11
29   invokespecial < Application, Lorg/apache/catalina/tribes/transport/bio/util/SingleRemoveSynchronizedAddLock, <init>()V > v9 @53 exception:v10(line 90)
BB12
30   putfield v1 = v9 < Application, Lorg/apache/catalina/tribes/transport/bio/util/FastQueue, lock, <Application,Lorg/apache/catalina/tribes/transport/bio/util/SingleRemoveSynchronizedAddLock> >(line 90)
BB13
32   v11 = getfield < Application, Lorg/apache/catalina/tribes/transport/bio/util/FastQueue, lock, <Application,Lorg/apache/catalina/tribes/transport/bio/util/SingleRemoveSynchronizedAddLock> > v1(line 91)
BB14
34   v12 = getfield < Application, Lorg/apache/catalina/tribes/transport/bio/util/FastQueue, addWaitTimeout, <Primordial,J> > v1(line 91)
BB15
35   invokevirtual < Application, Lorg/apache/catalina/tribes/transport/bio/util/SingleRemoveSynchronizedAddLock, setAddWaitTimeout(J)V > v11,v12 @67 exception:v13(line 91)
BB16
37   v14 = getfield < Application, Lorg/apache/catalina/tribes/transport/bio/util/FastQueue, lock, <Application,Lorg/apache/catalina/tribes/transport/bio/util/SingleRemoveSynchronizedAddLock> > v1(line 92)
BB17
39   v15 = getfield < Application, Lorg/apache/catalina/tribes/transport/bio/util/FastQueue, removeWaitTimeout, <Primordial,J> > v1(line 92)
BB18
40   invokevirtual < Application, Lorg/apache/catalina/tribes/transport/bio/util/SingleRemoveSynchronizedAddLock, setRemoveWaitTimeout(J)V > v14,v15 @78 exception:v16(line 92)
BB19
41   return                                  (line 93)
BB20

**CGNode:** Node: < Application, Lorg/apache/catalina/tribes/group/interceptors/MessageDispatchInterceptor, setOptionFlag(I)V > Context: ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,Lorg/apache/catalina/tribes/group/interceptors/MessageDispatchInterceptor>@11 in Everywhere} ]
**IR:** < Application, Lorg/apache/catalina/tribes/group/interceptors/MessageDispatchInterceptor, setOptionFlag(I)V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..2]
    -> BB3
    -> BB2
BB2[3..5]
    -> BB3
    -> BB5
BB3[6..8]
    -> BB4
    -> BB5
BB4[9..9]
    -> BB5
BB5[-1..-2]
Instructions:
BB0
BB1
2   conditional branch(eq) v2,v4:#8          (line 111)
BB2
3   v5 = getstatic < Application, Lorg/apache/catalina/tribes/group/interceptors/MessageDispatchInterceptor, log, <Application,Lorg/apache/juli/logging/Log> >(line 111)
5   invokeinterface < Application, Lorg/apache/juli/logging/Log, warn(Ljava/lang/Object;)V > v5,v6:#Warning, you are overriding the asynchronous option flag, this will disable the Channel.SEND_OPTIONS_ASYNCHRONOUS that other apps might use. @11 exception:v7(line 111)
BB3
8   invokespecial < Application, Lorg/apache/catalina/tribes/group/ChannelInterceptorBase, setOptionFlag(I)V > v1,v2 @18 exception:v8(line 112)
BB4
9   return                                   (line 113)
BB5

**CGNode:** Node: < Application, Lorg/apache/catalina/tribes/group/interceptors/MessageDispatchInterceptor, removeFromQueue()Lorg/apache/catalina/tribes/transport/bio/util/LinkObject; > Context: ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,Lorg/apache/catalina/tribes/group/interceptors/MessageDispatchInterceptor>@11 in Everywhere} ]
**IR:** < Application, Lorg/apache/catalina/tribes/group/interceptors/MessageDispatchInterceptor, removeFromQueue()Lorg/apache/catalina/tribes/transport/bio/util/LinkObject; >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..1]
    -> BB2
    -> BB4
BB2[2..2]
    -> BB3
    -> BB4
BB3[3..3]
    -> BB4
BB4[-1..-2]
Instructions:
BB0
BB1
1   v3 = getfield < Application, Lorg/apache/catalina/tribes/group/interceptors/MessageDispatchInterceptor, queue, <Application,Lorg/apache/catalina/tribes/transport/bio/util/FastQueue> > v1(line 88)
BB2
2   v5 = invokevirtual < Application, Lorg/apache/catalina/tribes/transport/bio/util/FastQueue, remove()Lorg/apache/catalina/tribes/transport/bio/util/LinkObject; > v3 @4 exception:v4(line 88)
BB3
3   return v5                                (line 88)
BB4

**CGNode:** Node: < Application, Lorg/apache/catalina/tribes/group/interceptors/MessageDispatchInterceptor, sendAsyncData(Lorg/apache/catalina/tribes/transport/bio/util/LinkObject;)Lorg/apache/catalina/tribes/transport/bio/util/LinkObject; > Context: ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,Lorg/apache/catalina/tribes/group/interceptors/MessageDispatchInterceptor>@11 in Everywhere} ]
**IR:** < Application, Lorg/apache/catalina/tribes/group/interceptors/MessageDispatchInterceptor, sendAsyncData(Lorg/apache/catalina/tribes/transport/bio/util/LinkObject;)Lorg/apache/catalina/tribes/transport/bio/util/LinkObject; >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..1]
    -> BB2
    -> BB48
BB2[2..4]
    -> BB3
    -> BB48
BB3[5..10]
    -> BB4
    -> BB14
    -> BB37
BB4[11..12]
    -> BB5
    -> BB12
    -> BB37
BB5[13..14]
    -> BB42
    -> BB6
BB6[15..16]
    -> BB7
    -> BB12
    -> BB37
BB7[17..17]
    -> BB8
    -> BB37
BB8[18..20]
    -> BB9
    -> BB12
    -> BB37
BB9[21..21]
    -> BB10
    -> BB12
    -> BB37
BB10[22..22]
    -> BB11
    -> BB12
    -> BB37
BB11[23..23]
    -> BB42
BB12[24..28]
    -> BB13
    -> BB14
    -> BB37
BB13[29..29]
    -> BB42
BB14[30..36]
    -> BB17
    -> BB15
BB15[37..38]
    -> BB16
    -> BB37
BB16[39..40]
    -> BB20
BB17[41..41]
    -> BB18
    -> BB37
BB18[42..44]
    -> BB19
    -> BB37
BB19[45..45]
    -> BB20
BB20[46..47]
    -> BB21
    -> BB37
BB21[48..49]
    -> BB23
    -> BB22
BB22[50..53]
    -> BB23
    -> BB37
BB23[54..55]
    -> BB24
    -> BB31
    -> BB37
BB24[56..57]
    -> BB32
    -> BB25
BB25[58..59]
    -> BB26
    -> BB31
    -> BB37
BB26[60..61]
    -> BB27
    -> BB37
BB27[62..64]
    -> BB28
    -> BB31
    -> BB37
BB28[65..65]
    -> BB29
    -> BB31
    -> BB37
BB29[66..66]
    -> BB30
    -> BB31
    -> BB37
BB30[67..67]
    -> BB32
BB31[68..72]
    -> BB32
    -> BB37
BB32[73..75]
    -> BB33
    -> BB48
BB33[76..76]
    -> BB34
    -> BB48
BB34[77..79]
    -> BB35
    -> BB48
BB35[80..82]
    -> BB36
    -> BB48
BB36[83..84]
    -> BB47
BB37[85..88]
    -> BB38
    -> BB48
BB38[89..89]
    -> BB39
    -> BB48
BB39[90..92]
    -> BB40
    -> BB48
BB40[93..95]
    -> BB41
    -> BB48
BB41[96..98]
    -> BB48
BB42[99..101]
    -> BB43
    -> BB48
BB43[102..102]
    -> BB44
    -> BB48
BB44[103..105]
    -> BB45
    -> BB48
BB45[106..108]
    -> BB46
    -> BB48
BB46[109..109]
    -> BB47
BB47[110..111]
    -> BB48
BB48[-1..-2]
Instructions:
BB0
BB1
1   v5 = invokevirtual < Application, Lorg/apache/catalina/tribes/transport/bio/util/LinkObject, data()Lorg/apache/catalina/tribes/ChannelMessage; > v2 @1 exception:v4(line 190)
BB2
4   v7 = invokevirtual < Application, Lorg/apache/catalina/tribes/transport/bio/util/LinkObject, getDestination()[Lorg/apache/catalina/tribes/Member; > v2 @6 exception:v6(line 191)
BB3
10   invokespecial < Application, Lorg/apache/catalina/tribes/group/ChannelInterceptorBase, sendMessage([Lorg/apache/catalina/tribes/Member;Lorg/apache/catalina/tribes/ChannelMessage;Lorg/apache/catalina/tribes/group/InterceptorPayload;)V > v1,v7,v5,v8:#null @14 exception:v9(line 193)
BB4
12   v11 = invokevirtual < Application, Lorg/apache/catalina/tribes/transport/bio/util/LinkObject, getHandler()Lorg/apache/catalina/tribes/ErrorHandler; > v2 @18 exception:v10(line 195)
BB5
14   conditional branch(eq) v11,v8:#null     (line 195)
BB6
16   v13 = invokevirtual < Application, Lorg/apache/catalina/tribes/transport/bio/util/LinkObject, getHandler()Lorg/apache/catalina/tribes/ErrorHandler; > v2 @25 exception:v12(line 195)
BB7
17   v14 = new <Application,Lorg/apache/catalina/tribes/UniqueId>@28(line 195)
BB8
20   v16 = invokeinterface < Application, Lorg/apache/catalina/tribes/ChannelMessage, getUniqueId()[B > v5 @33 exception:v15(line 195)
BB9
21   invokespecial < Application, Lorg/apache/catalina/tribes/UniqueId, <init>([B)V > v14,v16 @38 exception:v17(line 195)
BB10
22   invokeinterface < Application, Lorg/apache/catalina/tribes/ErrorHandler, handleCompletion(Lorg/apache/catalina/tribes/UniqueId;)V > v13,v14 @41 exception:v18(line 195)
BB11
23   goto                                    (line 195)
BB12<Handler>
           v19 = getCaughtException 
25   v20 = getstatic < Application, Lorg/apache/catalina/tribes/group/interceptors/MessageDispatchInterceptor, log, <Application,Lorg/apache/juli/logging/Log> >(line 197)
28   invokeinterface < Application, Lorg/apache/juli/logging/Log, error(Ljava/lang/Object;Ljava/lang/Throwable;)V > v20,v21:#Unable to report back completed message.,v19 @58 exception:v22(line 197)
BB13
29   goto                                    (line 197)
BB14<Handler>
           v23 = getCaughtException 
34   v24 = instanceof v23 <Application,Lorg/apache/catalina/tribes/ChannelException>(line 201)
36   conditional branch(eq) v24,v25:#0       (line 201)
BB15
38   v28 = checkcast <Application,Lorg/apache/catalina/tribes/ChannelException>v23(line 201)
BB16
40   goto                                    (line 201)
BB17
41   v26 = new <Application,Lorg/apache/catalina/tribes/ChannelException>@89(line 202)
BB18
44   invokespecial < Application, Lorg/apache/catalina/tribes/ChannelException, <init>(Ljava/lang/Throwable;)V > v26,v23 @95 exception:v27(line 202)
BB19
BB20
           v29 = phi  v28,v26
46   v30 = getstatic < Application, Lorg/apache/catalina/tribes/group/interceptors/MessageDispatchInterceptor, log, <Application,Lorg/apache/juli/logging/Log> >(line 203)
47   v32 = invokeinterface < Application, Lorg/apache/juli/logging/Log, isDebugEnabled()Z > v30 @103 exception:v31(line 203)
BB21
49   conditional branch(eq) v32,v25:#0       (line 203)
BB22
50   v33 = getstatic < Application, Lorg/apache/catalina/tribes/group/interceptors/MessageDispatchInterceptor, log, <Application,Lorg/apache/juli/logging/Log> >(line 203)
53   invokeinterface < Application, Lorg/apache/juli/logging/Log, debug(Ljava/lang/Object;Ljava/lang/Throwable;)V > v33,v34:#Error while processing async message.,v23 @118 exception:v35(line 203)
BB23
55   v37 = invokevirtual < Application, Lorg/apache/catalina/tribes/transport/bio/util/LinkObject, getHandler()Lorg/apache/catalina/tribes/ErrorHandler; > v2 @124 exception:v36(line 205)
BB24
57   conditional branch(eq) v37,v8:#null     (line 205)
BB25
59   v39 = invokevirtual < Application, Lorg/apache/catalina/tribes/transport/bio/util/LinkObject, getHandler()Lorg/apache/catalina/tribes/ErrorHandler; > v2 @131 exception:v38(line 205)
BB26
61   v40 = new <Application,Lorg/apache/catalina/tribes/UniqueId>@136(line 205)
BB27
64   v42 = invokeinterface < Application, Lorg/apache/catalina/tribes/ChannelMessage, getUniqueId()[B > v5 @141 exception:v41(line 205)
BB28
65   invokespecial < Application, Lorg/apache/catalina/tribes/UniqueId, <init>([B)V > v40,v42 @146 exception:v43(line 205)
BB29
66   invokeinterface < Application, Lorg/apache/catalina/tribes/ErrorHandler, handleError(Lorg/apache/catalina/tribes/ChannelException;Lorg/apache/catalina/tribes/UniqueId;)V > v39,v29,v40 @149 exception:v44(line 205)
BB30
67   goto                                    (line 205)
BB31<Handler>
           v45 = getCaughtException 
69   v46 = getstatic < Application, Lorg/apache/catalina/tribes/group/interceptors/MessageDispatchInterceptor, log, <Application,Lorg/apache/juli/logging/Log> >(line 207)
72   invokeinterface < Application, Lorg/apache/juli/logging/Log, error(Ljava/lang/Object;Ljava/lang/Throwable;)V > v46,v47:#Unable to report back error message.,v45 @167 exception:v48(line 207)
BB32
75   v63 = invokeinterface < Application, Lorg/apache/catalina/tribes/ChannelMessage, getMessage()Lorg/apache/catalina/tribes/io/XByteBuffer; > v5 @174 exception:v62(line 210)
BB33
76   v65 = invokevirtual < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, getLength()I > v63 @179 exception:v64(line 210)
BB34
77   v66 = neg v65                           (line 210)
78   v67 = conversion(J) v66                 (line 210)
79   v69 = invokevirtual < Application, Lorg/apache/catalina/tribes/group/interceptors/MessageDispatchInterceptor, addAndGetCurrentSize(J)J > v1,v67 @184 exception:v68(line 210)
BB35
82   v71 = invokevirtual < Application, Lorg/apache/catalina/tribes/transport/bio/util/LinkObject, next()Lorg/apache/catalina/tribes/transport/bio/util/LinkObject; > v2 @189 exception:v70(line 211)
BB36
84   goto                                    (line 211)
BB37<Handler>
           v49 = getCaughtException 
88   v53 = invokeinterface < Application, Lorg/apache/catalina/tribes/ChannelMessage, getMessage()Lorg/apache/catalina/tribes/io/XByteBuffer; > v5 @200 exception:v52(line 210)
BB38
89   v55 = invokevirtual < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, getLength()I > v53 @205 exception:v54(line 210)
BB39
90   v56 = neg v55                           (line 210)
91   v57 = conversion(J) v56                 (line 210)
92   v59 = invokevirtual < Application, Lorg/apache/catalina/tribes/group/interceptors/MessageDispatchInterceptor, addAndGetCurrentSize(J)J > v1,v57 @210 exception:v58(line 210)
BB40
95   v61 = invokevirtual < Application, Lorg/apache/catalina/tribes/transport/bio/util/LinkObject, next()Lorg/apache/catalina/tribes/transport/bio/util/LinkObject; > v2 @215 exception:v60(line 211)
BB41
98   throw v49                               (line 212)
BB42
101   v73 = invokeinterface < Application, Lorg/apache/catalina/tribes/ChannelMessage, getMessage()Lorg/apache/catalina/tribes/io/XByteBuffer; > v5 @224 exception:v72(line 210)
BB43
102   v75 = invokevirtual < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, getLength()I > v73 @229 exception:v74(line 210)
BB44
103   v76 = neg v75                          (line 210)
104   v77 = conversion(J) v76                (line 210)
105   v79 = invokevirtual < Application, Lorg/apache/catalina/tribes/group/interceptors/MessageDispatchInterceptor, addAndGetCurrentSize(J)J > v1,v77 @234 exception:v78(line 210)
BB45
108   v81 = invokevirtual < Application, Lorg/apache/catalina/tribes/transport/bio/util/LinkObject, next()Lorg/apache/catalina/tribes/transport/bio/util/LinkObject; > v2 @239 exception:v80(line 211)
BB46
BB47
           v82 = phi  v71,v81
111   return v82                             (line 213)
BB48

**CGNode:** Node: < Application, Lorg/apache/tomcat/util/net/NioBlockingSelector$BlockPoller, events()Z > Context: ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,Lorg/apache/tomcat/util/net/NioBlockingSelector$BlockPoller>@14 in Everywhere} ]
**IR:** < Application, Lorg/apache/tomcat/util/net/NioBlockingSelector$BlockPoller, events()Z >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..5]
    -> BB2
    -> BB14
BB2[6..6]
    -> BB3
    -> BB14
BB3[7..8]
    -> BB5
    -> BB4
BB4[9..10]
    -> BB6
BB5[11..11]
    -> BB6
BB6[12..13]
    -> BB9
BB7[14..15]
    -> BB8
    -> BB14
BB8[16..17]
    -> BB9
BB9[18..19]
    -> BB10
    -> BB14
BB10[20..20]
    -> BB11
    -> BB14
BB11[21..21]
    -> BB12
    -> BB14
BB12[22..25]
    -> BB7
    -> BB13
BB13[26..27]
    -> BB14
BB14[-1..-2]
Instructions:
BB0
BB1
5   v5 = getfield < Application, Lorg/apache/tomcat/util/net/NioBlockingSelector$BlockPoller, events, <Application,Ljava/util/concurrent/ConcurrentLinkedQueue> > v1(line 309)
BB2
6   v7 = invokevirtual < Application, Ljava/util/concurrent/ConcurrentLinkedQueue, size()I > v5 @8 exception:v6(line 309)
BB3
8   conditional branch(le) v7,v3:#0          (line 309)
BB4
10   goto                                    (line 309)
BB5
BB6
           v9 = phi  v8:#1,v3:#0
13   goto                                    (line 310)
BB7
15   invokeinterface < Application, Ljava/lang/Runnable, run()V > v13 @24 exception:v14(line 311)
BB8
BB9
           v15 = phi  v9,v8:#1
19   v10 = getfield < Application, Lorg/apache/tomcat/util/net/NioBlockingSelector$BlockPoller, events, <Application,Ljava/util/concurrent/ConcurrentLinkedQueue> > v1(line 310)
BB10
20   v12 = invokevirtual < Application, Ljava/util/concurrent/ConcurrentLinkedQueue, poll()Ljava/lang/Object; > v10 @35 exception:v11(line 310)
BB11
21   v13 = checkcast <Application,Ljava/lang/Runnable>v12(line 310)
BB12
25   conditional branch(ne) v13,v4:#null     (line 310)
BB13
27   return v15                              (line 314)
BB14

**CGNode:** Node: < Application, Lorg/apache/tomcat/util/net/NioBlockingSelector, access$0()Lorg/apache/juli/logging/Log; > Context: ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,Lorg/apache/tomcat/util/net/NioBlockingSelector$BlockPoller>@14 in Everywhere} ]
**IR:** < Application, Lorg/apache/tomcat/util/net/NioBlockingSelector, access$0()Lorg/apache/juli/logging/Log; >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..1]
    -> BB2
BB2[-1..-2]
Instructions:
BB0
BB1
0   v2 = getstatic < Application, Lorg/apache/tomcat/util/net/NioBlockingSelector, log, <Application,Lorg/apache/juli/logging/Log> >(line 43)
1   return v2                                (line 43)
BB2

**CGNode:** Node: < Application, Lorg/apache/tomcat/util/net/NioBlockingSelector, <clinit>()V > Context: Everywhere
**IR:** < Application, Lorg/apache/tomcat/util/net/NioBlockingSelector, <clinit>()V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..0]
    -> BB2
    -> BB4
BB2[1..1]
    -> BB3
    -> BB4
BB3[2..5]
    -> BB4
BB4[-1..-2]
Instructions:
BB0
BB1
0   v2 = load_metadata: <Primordial,Lorg/apache/tomcat/util/net/NioBlockingSelector>, <Primordial,Ljava/lang/Class>(line 43)
BB2
1   v4 = invokestatic < Application, Lorg/apache/juli/logging/LogFactory, getLog(Ljava/lang/Class;)Lorg/apache/juli/logging/Log; > v2 @2 exception:v3(line 43)
BB3
2   putstatic v4 < Application, Lorg/apache/tomcat/util/net/NioBlockingSelector, log, <Application,Lorg/apache/juli/logging/Log> >(line 43)
4   putstatic v5:#0 < Application, Lorg/apache/tomcat/util/net/NioBlockingSelector, threadCounter, <Primordial,I> >(line 45)
5   return                                   (line 41)
BB4

**CGNode:** Node: < Application, Lorg/apache/tomcat/util/ExceptionUtils, handleThrowable(Ljava/lang/Throwable;)V > Context: ReceiverStringContext: [ [<Primordial,Ljava/lang/NullPointerException>] ]
**IR:** < Application, Lorg/apache/tomcat/util/ExceptionUtils, handleThrowable(Ljava/lang/Throwable;)V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..3]
    -> BB4
    -> BB2
BB2[4..5]
    -> BB3
    -> BB8
BB3[6..6]
    -> BB8
BB4[7..10]
    -> BB7
    -> BB5
BB5[11..12]
    -> BB6
    -> BB8
BB6[13..13]
    -> BB8
BB7[14..14]
    -> BB8
BB8[-1..-2]
Instructions:
BB0
BB1
1   v3 = instanceof v1 <Application,Ljava/lang/ThreadDeath>(line 33)
3   conditional branch(eq) v3,v4:#0          (line 33)
BB2
5   v7 = checkcast <Application,Ljava/lang/ThreadDeath>v1(line 34)
BB3
6   throw v7                                 (line 34)
BB4
8   v5 = instanceof v1 <Application,Ljava/lang/VirtualMachineError>(line 36)
10   conditional branch(eq) v5,v4:#0         (line 36)
BB5
12   v6 = checkcast <Application,Ljava/lang/VirtualMachineError>v1(line 37)
BB6
13   throw v6                                (line 37)
BB7
14   return                                  (line 40)
BB8

**CGNode:** Node: < Application, Lorg/apache/tomcat/util/net/NioBlockingSelector$BlockPoller, countDown(Ljava/util/concurrent/CountDownLatch;)V > Context: ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,Lorg/apache/tomcat/util/net/NioBlockingSelector$BlockPoller>@14 in Everywhere} ]
**IR:** < Application, Lorg/apache/tomcat/util/net/NioBlockingSelector$BlockPoller, countDown(Ljava/util/concurrent/CountDownLatch;)V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..2]
    -> BB3
    -> BB2
BB2[3..3]
    -> BB5
BB3[4..5]
    -> BB4
    -> BB5
BB4[6..6]
    -> BB5
BB5[-1..-2]
Instructions:
BB0
BB1
2   conditional branch(ne) v2,v4:#null       (line 390)
BB2
3   return                                   (line 390)
BB3
5   invokevirtual < Application, Ljava/util/concurrent/CountDownLatch, countDown()V > v2 @6 exception:v5(line 391)
BB4
6   return                                   (line 392)
BB5

**CGNode:** Node: < Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive$1, run()V > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, main([Ljava/lang/String;)V >:NEW <Application,Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive$1>@68 in ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,[Ljava/lang/String>@1 in Everywhere} ]} ]
**IR:** < Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive$1, run()V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..1]
    -> BB2
    -> BB4
    -> BB5
BB2[2..7]
    -> BB3
    -> BB4
    -> BB5
BB3[8..8]
    -> BB1
BB4[9..10]
    -> BB1
BB5[-1..-2]
Instructions:
BB0
BB1
1   invokestatic < Application, Ljava/lang/Thread, sleep(J)V > v3:#1000 @3 exception:v4(line 56)
BB2
2   v5 = getstatic < Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, start, <Primordial,J> >(line 57)
3   v6 = getstatic < Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, mb, <Primordial,D> >(line 57)
4   v7 = getstatic < Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, count, <Primordial,I> >(line 57)
5   v8 = getstatic < Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, df, <Application,Ljava/text/DecimalFormat> >(line 57)
6   v9 = getstatic < Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, total, <Application,Ljava/math/BigDecimal> >(line 57)
7   invokestatic < Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, access$0(JDILjava/text/DecimalFormat;Ljava/math/BigDecimal;)V > v5,v6,v7,v8,v9 @21 exception:v10(line 57)
BB3
8   goto                                     (line 57)
BB4<Handler>
           v11 = getCaughtException 
10   goto                                    (line 54)
BB5

**CGNode:** Node: < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, expand(I)V > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, main([Ljava/lang/String;)V >:NEW <Application,Lorg/apache/catalina/tribes/io/XByteBuffer>@19 in ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,[Ljava/lang/String>@1 in Everywhere} ]} ]
**IR:** < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, expand(I)V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..1]
    -> BB2
    -> BB10
BB2[2..2]
    -> BB3
    -> BB10
BB3[3..6]
    -> BB4
    -> BB10
BB4[7..7]
    -> BB5
    -> BB10
BB5[8..10]
    -> BB6
    -> BB10
BB6[11..15]
    -> BB7
    -> BB10
BB7[16..16]
    -> BB8
    -> BB10
BB8[17..19]
    -> BB9
    -> BB10
BB9[20..20]
    -> BB10
BB10[-1..-2]
Instructions:
BB0
BB1
1   v4 = getfield < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, buf, <Primordial,[B> > v1(line 239)
BB2
2   v5 = arraylength v4                      (line 239)
BB3
4   v7 = binaryop(SHL) v5 , v6:#1            (line 239)
6   v9 = invokestatic < Application, Ljava/lang/Math, max(II)I > v7,v2 @8 exception:v8(line 239)
BB4
7   v10 = new <Primordial,[B>@11v9           (line 239)
BB5
10   v11 = getfield < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, buf, <Primordial,[B> > v1(line 240)
BB6
15   v13 = getfield < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, bufSize, <Primordial,I> > v1(line 240)
BB7
16   invokestatic < Application, Ljava/lang/System, arraycopy(Ljava/lang/Object;ILjava/lang/Object;II)V > v11,v12:#0,v10,v12:#0,v13 @25 exception:v14(line 240)
BB8
19   putfield v1 = v10 < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, buf, <Primordial,[B> >(line 241)
BB9
20   return                                  (line 242)
BB10

**CGNode:** Node: < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, firstIndexOf([BI[B)I > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/io/XByteBuffer, <init>(IZ)V >:NEW <Primordial,[B>@21 in ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, main([Ljava/lang/String;)V >:NEW <Application,Lorg/apache/catalina/tribes/io/XByteBuffer>@19 in ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,[Ljava/lang/String>@1 in Everywhere} ]} ]} ]
**IR:** < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, firstIndexOf([BI[B)I >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..3]
    -> BB2
    -> BB45
BB2[4..5]
    -> BB3
    -> BB45
BB3[6..6]
    -> BB5
    -> BB4
BB4[7..8]
    -> BB45
BB5[9..10]
    -> BB6
    -> BB45
BB6[11..12]
    -> BB9
    -> BB7
BB7[13..14]
    -> BB8
    -> BB45
BB8[15..16]
    -> BB10
    -> BB9
BB9[17..18]
    -> BB45
BB10[19..21]
    -> BB11
    -> BB45
BB11[22..22]
    -> BB15
    -> BB12
BB12[23..23]
    -> BB13
    -> BB45
BB13[24..25]
    -> BB14
    -> BB45
BB14[26..26]
    -> BB45
BB15[27..30]
    -> BB16
    -> BB45
BB16[31..33]
    -> BB17
    -> BB45
BB17[34..37]
    -> BB18
    -> BB45
BB18[38..41]
    -> BB43
BB19[42..45]
    -> BB20
    -> BB45
BB20[46..46]
    -> BB22
    -> BB21
BB21[47..47]
    -> BB24
BB22[48..51]
    -> BB23
BB23[52..54]
    -> BB19
    -> BB24
BB24[55..57]
    -> BB26
    -> BB25
BB25[58..59]
    -> BB45
BB26[60..64]
    -> BB28
    -> BB27
BB27[65..66]
    -> BB45
BB28[67..71]
    -> BB36
BB29[72..74]
    -> BB34
    -> BB30
BB30[75..77]
    -> BB31
    -> BB45
BB31[78..82]
    -> BB32
    -> BB45
BB32[83..83]
    -> BB34
    -> BB33
BB33[84..85]
    -> BB35
BB34[86..86]
    -> BB35
BB35[87..91]
    -> BB36
BB36[92..94]
    -> BB38
    -> BB37
BB37[95..97]
    -> BB29
    -> BB38
BB38[98..100]
    -> BB40
    -> BB39
BB39[101..103]
    -> BB43
BB40[104..108]
    -> BB42
    -> BB41
BB41[109..110]
    -> BB45
BB42[111..114]
    -> BB43
BB43[115..117]
    -> BB23
    -> BB44
BB44[118..119]
    -> BB45
BB45[-1..-2]
Instructions:
BB0
BB1
3   v6 = arraylength v3                      (line 510)
BB2
5   v7 = arraylength v1                      (line 510)
BB3
6   conditional branch(le) v6,v7             (line 510)
BB4
8   return v5:#-1                            (line 510)
BB5
10   v8 = arraylength v3                     (line 511)
BB6
12   conditional branch(eq) v8,v9:#0         (line 511)
BB7
14   v10 = arraylength v1                    (line 511)
BB8
16   conditional branch(ne) v10,v9:#0        (line 511)
BB9
18   return v5:#-1                           (line 511)
BB10
21   v11 = arraylength v1                    (line 512)
BB11
22   conditional branch(lt) v2,v11           (line 512)
BB12
23   v35 = new <Application,Ljava/lang/ArrayIndexOutOfBoundsException>@29(line 512)
BB13
25   invokespecial < Application, Ljava/lang/ArrayIndexOutOfBoundsException, <init>()V > v35 @33 exception:v36(line 512)
BB14
26   throw v35                               (line 512)
BB15
30   v12 = arraylength v1                    (line 514)
BB16
33   v13 = arraylength v3                    (line 515)
BB17
37   v14 = arrayload v3[v9:#0]               (line 516)
BB18
41   goto                                    (line 518)
BB19
45   v15 = arrayload v1[v18]                 (line 521)
BB20
46   conditional branch(ne) v14,v15          (line 521)
BB21
47   goto                                    (line 522)
BB22
50   v17 = binaryop(add) v18 , v16:#1        (line 523)
BB23
           v30 = phi  v27,v30
           v18 = phi  v29,v17
54   conditional branch(lt) v18,v12          (line 520)
BB24
57   conditional branch(lt) v18,v12          (line 525)
BB25
59   return v5:#-1                           (line 526)
BB26
62   v19 = binaryop(sub) v12 , v18           (line 530)
64   conditional branch(ge) v19,v13          (line 530)
BB27
66   return v5:#-1                           (line 531)
BB28
71   goto                                    (line 534)
BB29
74   conditional branch(eq) v25,v9:#0        (line 535)
BB30
77   v20 = arrayload v3[v26]                 (line 535)
BB31
81   v21 = binaryop(add) v18 , v26           (line 535)
82   v22 = arrayload v1[v21]                 (line 535)
BB32
83   conditional branch(ne) v20,v22          (line 535)
BB33
85   goto                                    (line 535)
BB34
BB35
           v23 = phi  v16:#1,v9:#0
90   v24 = binaryop(add) v26 , v16:#1        (line 534)
BB36
           v32 = phi  v30,v32
           v25 = phi  v16:#1,v23
           v26 = phi  v16:#1,v24
94   conditional branch(ge) v26,v13          (line 534)
BB37
97   conditional branch(ne) v25,v9:#0        (line 534)
BB38
100   conditional branch(eq) v25,v9:#0       (line 536)
BB39
103   goto                                   (line 537)
BB40
106   v33 = binaryop(sub) v12 , v18          (line 538)
108   conditional branch(ge) v33,v13         (line 538)
BB41
110   return v5:#-1                          (line 539)
BB42
113   v34 = binaryop(add) v18 , v16:#1       (line 541)
BB43
           v27 = phi  v5:#-1,v18,v32
           v28 = phi  v9:#0,v25,v25
           v29 = phi  v2,v18,v34
117   conditional branch(eq) v28,v9:#0       (line 518)
BB44
119   return v27                             (line 543)
BB45

**CGNode:** Node: < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, extractDataPackage(Z)Lorg/apache/catalina/tribes/io/XByteBuffer; > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, main([Ljava/lang/String;)V >:NEW <Application,Lorg/apache/catalina/tribes/io/XByteBuffer>@19 in ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,[Ljava/lang/String>@1 in Everywhere} ]} ]
**IR:** < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, extractDataPackage(Z)Lorg/apache/catalina/tribes/io/XByteBuffer; >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..2]
    -> BB2
    -> BB26
BB2[3..6]
    -> BB6
    -> BB3
BB3[7..7]
    -> BB4
    -> BB26
BB4[8..10]
    -> BB5
    -> BB26
BB5[11..11]
    -> BB26
BB6[12..13]
    -> BB7
    -> BB26
BB7[14..15]
    -> BB8
    -> BB26
BB8[16..16]
    -> BB9
    -> BB26
BB9[17..18]
    -> BB10
    -> BB26
BB10[19..21]
    -> BB11
    -> BB26
BB11[22..25]
    -> BB12
    -> BB26
BB12[26..27]
    -> BB13
    -> BB26
BB13[28..29]
    -> BB14
    -> BB26
BB14[30..33]
    -> BB15
    -> BB26
BB15[34..36]
    -> BB16
    -> BB26
BB16[37..39]
    -> BB25
    -> BB17
BB17[40..41]
    -> BB18
    -> BB26
BB18[42..47]
    -> BB19
    -> BB26
BB19[48..52]
    -> BB20
    -> BB26
BB20[53..55]
    -> BB21
    -> BB26
BB21[56..57]
    -> BB22
    -> BB26
BB22[58..60]
    -> BB23
    -> BB26
BB23[61..63]
    -> BB24
    -> BB26
BB24[64..64]
    -> BB25
    -> BB26
BB25[65..66]
    -> BB26
BB26[-1..-2]
Instructions:
BB0
BB1
2   v6 = invokevirtual < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, countPackages(Z)I > v1,v4:#1 @2 exception:v5(line 307)
BB2
6   conditional branch(ne) v6,v7:#0          (line 308)
BB3
7   v39 = new <Application,Ljava/lang/IllegalStateException>@10(line 309)
BB4
10   invokespecial < Application, Ljava/lang/IllegalStateException, <init>(Ljava/lang/String;)V > v39,v40:#No package exists in XByteBuffer @16 exception:v41(line 309)
BB5
11   throw v39                               (line 309)
BB6
13   v8 = getfield < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, buf, <Primordial,[B> > v1(line 311)
BB7
14   v9 = getstatic < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, START_DATA, <Primordial,[B> >(line 311)
15   v10 = arraylength v9                    (line 311)
BB8
16   v12 = invokestatic < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, toInt([BI)I > v8,v10 @28 exception:v11(line 311)
BB9
18   v14 = invokestatic < Application, Lorg/apache/catalina/tribes/io/BufferPool, getBufferPool()Lorg/apache/catalina/tribes/io/BufferPool; > @32 exception:v13(line 312)
BB10
21   v16 = invokevirtual < Application, Lorg/apache/catalina/tribes/io/BufferPool, getBuffer(IZ)Lorg/apache/catalina/tribes/io/XByteBuffer; > v14,v12,v7:#0 @37 exception:v15(line 312)
BB11
25   invokevirtual < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, setLength(I)V > v16,v12 @45 exception:v17(line 313)
BB12
27   v18 = getfield < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, buf, <Primordial,[B> > v1(line 314)
BB13
28   v19 = getstatic < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, START_DATA, <Primordial,[B> >(line 314)
29   v20 = arraylength v19                   (line 314)
BB14
31   v22 = binaryop(add) v20 , v21:#4        (line 314)
33   v24 = invokevirtual < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, getBytesDirect()[B > v16 @60 exception:v23(line 314)
BB15
36   invokestatic < Application, Ljava/lang/System, arraycopy(Ljava/lang/Object;ILjava/lang/Object;II)V > v18,v22,v24,v7:#0,v12 @65 exception:v25(line 314)
BB16
39   conditional branch(eq) v2,v7:#0         (line 315)
BB17
40   v26 = getstatic < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, START_DATA, <Primordial,[B> >(line 316)
41   v27 = arraylength v26                   (line 316)
BB18
43   v28 = binaryop(add) v27 , v21:#4        (line 316)
45   v29 = binaryop(add) v28 , v12           (line 316)
46   v30 = getstatic < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, END_DATA, <Primordial,[B> >(line 316)
47   v31 = arraylength v30                   (line 316)
BB19
48   v32 = binaryop(add) v29 , v31           (line 316)
52   v33 = getfield < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, bufSize, <Primordial,I> > v1(line 317)
BB20
54   v34 = binaryop(sub) v33 , v32           (line 317)
55   putfield v1 = v34 < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, bufSize, <Primordial,I> >(line 317)
BB21
57   v35 = getfield < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, buf, <Primordial,[B> > v1(line 318)
BB22
60   v36 = getfield < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, buf, <Primordial,[B> > v1(line 318)
BB23
63   v37 = getfield < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, bufSize, <Primordial,I> > v1(line 318)
BB24
64   invokestatic < Application, Ljava/lang/System, arraycopy(Ljava/lang/Object;ILjava/lang/Object;II)V > v35,v32,v36,v7:#0,v37 @113 exception:v38(line 318)
BB25
66   return v16                              (line 320)
BB26

**CGNode:** Node: < Application, Lorg/apache/catalina/tribes/io/ChannelData, getDataFromPackage(Lorg/apache/catalina/tribes/io/XByteBuffer;)Lorg/apache/catalina/tribes/io/ChannelData; > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, main([Ljava/lang/String;)V >:NEW <Application,Lorg/apache/catalina/tribes/io/XByteBuffer>@19 in ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,[Ljava/lang/String>@1 in Everywhere} ]} ]
**IR:** < Application, Lorg/apache/catalina/tribes/io/ChannelData, getDataFromPackage(Lorg/apache/catalina/tribes/io/XByteBuffer;)Lorg/apache/catalina/tribes/io/ChannelData; >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..0]
    -> BB2
    -> BB33
BB2[1..3]
    -> BB3
    -> BB33
BB3[4..9]
    -> BB4
    -> BB33
BB4[10..11]
    -> BB5
    -> BB33
BB5[12..12]
    -> BB6
    -> BB33
BB6[13..19]
    -> BB7
    -> BB33
BB7[20..21]
    -> BB8
    -> BB33
BB8[22..22]
    -> BB9
    -> BB33
BB9[23..29]
    -> BB10
    -> BB33
BB10[30..31]
    -> BB11
    -> BB33
BB11[32..32]
    -> BB12
    -> BB33
BB12[33..33]
    -> BB13
    -> BB33
BB13[34..39]
    -> BB14
    -> BB33
BB14[40..42]
    -> BB15
    -> BB33
BB15[43..45]
    -> BB16
    -> BB33
BB16[46..46]
    -> BB17
    -> BB33
BB17[47..47]
    -> BB18
    -> BB33
BB18[48..50]
    -> BB19
    -> BB33
BB19[51..51]
    -> BB20
    -> BB33
BB20[52..55]
    -> BB21
    -> BB33
BB21[56..57]
    -> BB22
    -> BB33
BB22[58..65]
    -> BB23
    -> BB33
BB23[66..68]
    -> BB24
    -> BB33
BB24[69..69]
    -> BB25
    -> BB33
BB25[70..75]
    -> BB26
    -> BB33
BB26[76..77]
    -> BB27
    -> BB33
BB27[78..84]
    -> BB28
    -> BB33
BB28[85..87]
    -> BB29
    -> BB33
BB29[88..90]
    -> BB30
    -> BB33
BB30[91..93]
    -> BB31
    -> BB33
BB31[94..96]
    -> BB32
    -> BB33
BB32[97..98]
    -> BB33
BB33[-1..-2]
Instructions:
BB0
BB1
0   v3 = new <Application,Lorg/apache/catalina/tribes/io/ChannelData>@0(line 234)
BB2
3   invokespecial < Application, Lorg/apache/catalina/tribes/io/ChannelData, <init>(Z)V > v3,v4:#0 @5 exception:v5(line 234)
BB3
9   v7 = invokevirtual < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, getBytesDirect()[B > v1 @13 exception:v6(line 236)
BB4
11   v9 = invokestatic < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, toInt([BI)I > v7,v4:#0 @17 exception:v8(line 236)
BB5
12   invokevirtual < Application, Lorg/apache/catalina/tribes/io/ChannelData, setOptions(I)V > v3,v9 @20 exception:v10(line 236)
BB6
15   v12 = binaryop(add) v4:#0 , v11:#4      (line 237)
19   v14 = invokevirtual < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, getBytesDirect()[B > v1 @28 exception:v13(line 238)
BB7
21   v16 = invokestatic < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, toLong([BI)J > v14,v12 @32 exception:v15(line 238)
BB8
22   invokevirtual < Application, Lorg/apache/catalina/tribes/io/ChannelData, setTimestamp(J)V > v3,v16 @35 exception:v17(line 238)
BB9
25   v19 = binaryop(add) v12 , v18:#8        (line 239)
29   v21 = invokevirtual < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, getBytesDirect()[B > v1 @43 exception:v20(line 240)
BB10
31   v23 = invokestatic < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, toInt([BI)I > v21,v19 @47 exception:v22(line 240)
BB11
32   v24 = new <Primordial,[B>@50v23         (line 240)
BB12
33   putfield v3 = v24 < Application, Lorg/apache/catalina/tribes/io/ChannelData, uniqueId, <Primordial,[B> >(line 240)
BB13
36   v25 = binaryop(add) v19 , v11:#4        (line 241)
39   v27 = invokevirtual < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, getBytesDirect()[B > v1 @59 exception:v26(line 242)
BB14
42   v28 = getfield < Application, Lorg/apache/catalina/tribes/io/ChannelData, uniqueId, <Primordial,[B> > v3(line 242)
BB15
45   v29 = getfield < Application, Lorg/apache/catalina/tribes/io/ChannelData, uniqueId, <Primordial,[B> > v3(line 242)
BB16
46   v30 = arraylength v29                   (line 242)
BB17
47   invokestatic < Application, Ljava/lang/System, arraycopy(Ljava/lang/Object;ILjava/lang/Object;II)V > v27,v25,v28,v4:#0,v30 @73 exception:v31(line 242)
BB18
50   v32 = getfield < Application, Lorg/apache/catalina/tribes/io/ChannelData, uniqueId, <Primordial,[B> > v3(line 243)
BB19
51   v33 = arraylength v32                   (line 243)
BB20
52   v34 = binaryop(add) v25 , v33           (line 243)
55   v36 = invokevirtual < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, getBytesDirect()[B > v1 @85 exception:v35(line 245)
BB21
57   v38 = invokestatic < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, toInt([BI)I > v36,v34 @89 exception:v37(line 245)
BB22
61   v39 = binaryop(add) v34 , v11:#4        (line 246)
65   v41 = invokevirtual < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, getBytesDirect()[B > v1 @98 exception:v40(line 248)
BB23
68   v43 = invokestatic < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, getMember([BII)Lorg/apache/catalina/tribes/membership/MemberImpl; > v41,v39,v38 @103 exception:v42(line 248)
BB24
69   invokevirtual < Application, Lorg/apache/catalina/tribes/io/ChannelData, setAddress(Lorg/apache/catalina/tribes/Member;)V > v3,v43 @106 exception:v44(line 248)
BB25
72   v45 = binaryop(add) v39 , v38           (line 250)
75   v47 = invokevirtual < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, getBytesDirect()[B > v1 @114 exception:v46(line 251)
BB26
77   v49 = invokestatic < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, toInt([BI)I > v47,v45 @118 exception:v48(line 251)
BB27
81   v50 = binaryop(add) v45 , v11:#4        (line 252)
84   v52 = invokevirtual < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, getBytesDirect()[B > v1 @127 exception:v51(line 253)
BB28
87   v54 = invokevirtual < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, getBytesDirect()[B > v1 @132 exception:v53(line 253)
BB29
90   invokestatic < Application, Ljava/lang/System, arraycopy(Ljava/lang/Object;ILjava/lang/Object;II)V > v52,v50,v54,v4:#0,v49 @138 exception:v55(line 253)
BB30
93   invokevirtual < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, setLength(I)V > v1,v49 @144 exception:v56(line 254)
BB31
96   putfield v3 = v1 < Application, Lorg/apache/catalina/tribes/io/ChannelData, message, <Application,Lorg/apache/catalina/tribes/io/XByteBuffer> >(line 255)
BB32
98   return v3                               (line 256)
BB33

**CGNode:** Node: < Application, Lorg/apache/catalina/tribes/io/ChannelData, <clinit>()V > Context: Everywhere
**IR:** < Application, Lorg/apache/catalina/tribes/io/ChannelData, <clinit>()V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..1]
    -> BB2
    -> BB3
BB2[2..5]
    -> BB3
BB3[-1..-2]
Instructions:
BB0
BB1
1   v3 = new <Application,[Lorg/apache/catalina/tribes/io/ChannelData>@1v2:#0 (line 41)
BB2
2   putstatic v3 < Application, Lorg/apache/catalina/tribes/io/ChannelData, EMPTY_DATA_ARRAY, <Application,[Lorg/apache/catalina/tribes/io/ChannelData> >(line 41)
4   putstatic v2:#0 < Application, Lorg/apache/catalina/tribes/io/ChannelData, USE_SECURE_RANDOM_FOR_UUID, <Primordial,Z> >(line 43)
5   return                                   (line 38)
BB3

**CGNode:** Node: < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, toInt([BI)I > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/io/XByteBuffer, <init>(IZ)V >:NEW <Primordial,[B>@21 in ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, main([Ljava/lang/String;)V >:NEW <Application,Lorg/apache/catalina/tribes/io/XByteBuffer>@19 in ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,[Ljava/lang/String>@1 in Everywhere} ]} ]} ]
**IR:** < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, toInt([BI)I >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..4]
    -> BB2
    -> BB6
BB2[5..11]
    -> BB3
    -> BB6
BB3[12..21]
    -> BB4
    -> BB6
BB4[22..31]
    -> BB5
    -> BB6
BB5[32..37]
    -> BB6
BB6[-1..-2]
Instructions:
BB0
BB1
3   v5 = binaryop(add) v2 , v4:#3            (line 396)
4   v6 = arrayload v1[v5]                    (line 396)
BB2
6   v8 = binaryop(and) v6 , v7:#255          (line 396)
10   v10 = binaryop(add) v2 , v9:#2          (line 397)
11   v11 = arrayload v1[v10]                 (line 397)
BB3
13   v12 = binaryop(and) v11 , v7:#255       (line 397)
15   v14 = binaryop(SHL) v12 , v13:#8        (line 397)
16   v15 = binaryop(add) v8 , v14            (line 396)
20   v17 = binaryop(add) v2 , v16:#1         (line 398)
21   v18 = arrayload v1[v17]                 (line 398)
BB4
23   v19 = binaryop(and) v18 , v7:#255       (line 398)
25   v21 = binaryop(SHL) v19 , v20:#16       (line 398)
26   v22 = binaryop(add) v15 , v21           (line 396)
30   v24 = binaryop(add) v2 , v23:#0         (line 399)
31   v25 = arrayload v1[v24]                 (line 399)
BB5
33   v26 = binaryop(and) v25 , v7:#255       (line 399)
35   v28 = binaryop(SHL) v26 , v27:#24       (line 399)
36   v29 = binaryop(add) v22 , v28           (line 396)
37   return v29                              (line 396)
BB6

**CGNode:** Node: < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, <init>()V > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, main([Ljava/lang/String;)V >:NEW <Application,Lorg/apache/tomcat/util/net/AprEndpoint>@0 in ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,[Ljava/lang/String>@6 in Everywhere} ]} ]
**IR:** < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, <init>()V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..1]
    -> BB2
    -> BB63
BB2[2..4]
    -> BB3
    -> BB63
BB3[5..7]
    -> BB4
    -> BB63
BB4[8..10]
    -> BB5
    -> BB63
BB5[11..13]
    -> BB6
    -> BB63
BB6[14..15]
    -> BB7
    -> BB63
BB7[16..17]
    -> BB8
    -> BB63
BB8[18..18]
    -> BB9
    -> BB63
BB9[19..21]
    -> BB10
    -> BB63
BB10[22..24]
    -> BB11
    -> BB63
BB11[25..27]
    -> BB12
    -> BB63
BB12[28..30]
    -> BB13
    -> BB63
BB13[31..33]
    -> BB14
    -> BB63
BB14[34..36]
    -> BB15
    -> BB63
BB15[37..39]
    -> BB16
    -> BB63
BB16[40..42]
    -> BB17
    -> BB63
BB17[43..45]
    -> BB18
    -> BB63
BB18[46..48]
    -> BB19
    -> BB63
BB19[49..51]
    -> BB20
    -> BB63
BB20[52..54]
    -> BB21
    -> BB63
BB21[55..57]
    -> BB22
    -> BB63
BB22[58..60]
    -> BB23
    -> BB63
BB23[61..63]
    -> BB24
    -> BB63
BB24[64..65]
    -> BB25
    -> BB63
BB25[66..67]
    -> BB26
    -> BB63
BB26[68..68]
    -> BB27
    -> BB63
BB27[69..70]
    -> BB28
    -> BB63
BB28[71..71]
    -> BB29
    -> BB63
BB29[72..74]
    -> BB30
    -> BB63
BB30[75..76]
    -> BB31
    -> BB63
BB31[77..79]
    -> BB32
    -> BB63
BB32[80..80]
    -> BB33
    -> BB63
BB33[81..81]
    -> BB34
    -> BB63
BB34[82..83]
    -> BB35
    -> BB63
BB35[84..84]
    -> BB36
    -> BB63
BB36[85..85]
    -> BB37
    -> BB63
BB37[86..88]
    -> BB38
    -> BB63
BB38[89..91]
    -> BB39
    -> BB63
BB39[92..94]
    -> BB40
    -> BB63
BB40[95..97]
    -> BB41
    -> BB63
BB41[98..100]
    -> BB42
    -> BB63
BB42[101..103]
    -> BB43
    -> BB63
BB43[104..104]
    -> BB44
    -> BB63
BB44[105..107]
    -> BB45
    -> BB63
BB45[108..110]
    -> BB46
    -> BB63
BB46[111..113]
    -> BB47
    -> BB63
BB47[114..114]
    -> BB48
    -> BB63
BB48[115..117]
    -> BB49
    -> BB63
BB49[118..118]
    -> BB50
    -> BB63
BB50[119..121]
    -> BB51
    -> BB63
BB51[122..122]
    -> BB52
    -> BB63
BB52[123..125]
    -> BB53
    -> BB63
BB53[126..128]
    -> BB54
    -> BB63
BB54[129..131]
    -> BB55
    -> BB63
BB55[132..134]
    -> BB56
    -> BB63
BB56[135..137]
    -> BB57
    -> BB63
BB57[138..140]
    -> BB58
    -> BB63
BB58[141..143]
    -> BB59
    -> BB63
BB59[144..146]
    -> BB60
    -> BB63
BB60[147..149]
    -> BB61
    -> BB63
BB61[150..150]
    -> BB62
    -> BB63
BB62[151..151]
    -> BB63
BB63[-1..-2]
Instructions:
BB0
BB1
1   invokespecial < Application, Ljava/lang/Object, <init>()V > v1 @1 exception:v3(line 48)
BB2
4   putfield v1 = v4:#0 < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, running, <Primordial,Z> >(line 108)
BB3
7   putfield v1 = v4:#0 < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, paused, <Primordial,Z> >(line 114)
BB4
10   putfield v1 = v4:#0 < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, internalExecutor, <Primordial,Z> >(line 119)
BB5
13   putfield v1 = v5:#null < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, connectionLimitLatch, <Application,Lorg/apache/tomcat/util/threads/LimitLatch> >(line 124)
BB6
15   v6 = new <Application,Lorg/apache/tomcat/util/net/SocketProperties>@25(line 129)
BB7
17   invokespecial < Application, Lorg/apache/tomcat/util/net/SocketProperties, <init>()V > v6 @29 exception:v7(line 129)
BB8
18   putfield v1 = v6 < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, socketProperties, <Application,Lorg/apache/tomcat/util/net/SocketProperties> >(line 129)
BB9
21   putfield v1 = v4:#0 < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, acceptorThreadCount, <Primordial,I> >(line 145)
BB10
24   putfield v1 = v8:#5 < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, acceptorThreadPriority, <Primordial,I> >(line 155)
BB11
27   putfield v1 = v9:#10000 < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, maxConnections, <Primordial,I> >(line 162)
BB12
30   putfield v1 = v5:#null < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, executor, <Application,Ljava/util/concurrent/Executor> >(line 176)
BB13
33   putfield v1 = v10:#100 < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, backlog, <Primordial,I> >(line 205)
BB14
36   putfield v1 = v11:#1 < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, bindOnInit, <Primordial,Z> >(line 215)
BB15
38   v12 = getstatic < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint$BindState, UNBOUND, <Application,Lorg/apache/tomcat/util/net/AbstractEndpoint$BindState> >(line 218)
39   putfield v1 = v12 < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, bindState, <Application,Lorg/apache/tomcat/util/net/AbstractEndpoint$BindState> >(line 218)
BB16
42   putfield v1 = v5:#null < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, keepAliveTimeout, <Application,Ljava/lang/Integer> >(line 223)
BB17
45   putfield v1 = v4:#0 < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, SSLEnabled, <Primordial,Z> >(line 262)
BB18
48   putfield v1 = v13:#10 < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, minSpareThreads, <Primordial,I> >(line 267)
BB19
51   putfield v1 = v14:#200 < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, maxThreads, <Primordial,I> >(line 285)
BB20
54   putfield v1 = v10:#100 < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, maxKeepAliveRequests, <Primordial,I> >(line 313)
BB21
57   putfield v1 = v15:#TP < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, name, <Application,Ljava/lang/String> >(line 324)
BB22
60   putfield v1 = v11:#1 < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, daemon, <Primordial,Z> >(line 333)
BB23
63   putfield v1 = v8:#5 < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, threadPriority, <Primordial,I> >(line 341)
BB24
65   v16 = new <Application,Ljava/util/HashMap>@121(line 356)
BB25
67   invokespecial < Application, Ljava/util/HashMap, <init>()V > v16 @125 exception:v17(line 356)
BB26
68   putfield v1 = v16 < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, attributes, <Application,Ljava/util/HashMap> >(line 356)
BB27
70   v19 = invokestatic < Application, Ljavax/net/ssl/KeyManagerFactory, getDefaultAlgorithm()Ljava/lang/String; > @132 exception:v18(line 727)
BB28
71   putfield v1 = v19 < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, algorithm, <Application,Ljava/lang/String> >(line 727)
BB29
74   putfield v1 = v20:#false < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, clientAuth, <Application,Ljava/lang/String> >(line 731)
BB30
76   v21 = new <Application,Ljava/lang/StringBuilder>@145(line 735)
BB31
79   v24 = invokestatic < Application, Ljava/lang/System, getProperty(Ljava/lang/String;)Ljava/lang/String; > v22:#user.home @151 exception:v23(line 735)
BB32
80   v26 = invokestatic < Application, Ljava/lang/String, valueOf(Ljava/lang/Object;)Ljava/lang/String; > v24 @154 exception:v25(line 735)
BB33
81   invokespecial < Application, Ljava/lang/StringBuilder, <init>(Ljava/lang/String;)V > v21,v26 @157 exception:v27(line 735)
BB34
83   v30 = invokevirtual < Application, Ljava/lang/StringBuilder, append(Ljava/lang/String;)Ljava/lang/StringBuilder; > v21,v28:#/.keystore @162 exception:v29(line 735)
BB35
84   v32 = invokevirtual < Application, Ljava/lang/StringBuilder, toString()Ljava/lang/String; > v30 @165 exception:v31(line 735)
BB36
85   putfield v1 = v32 < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, keystoreFile, <Application,Ljava/lang/String> >(line 735)
BB37
88   putfield v1 = v5:#null < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, keystorePass, <Application,Ljava/lang/String> >(line 743)
BB38
91   putfield v1 = v33:#JKS < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, keystoreType, <Application,Ljava/lang/String> >(line 747)
BB39
94   putfield v1 = v5:#null < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, keystoreProvider, <Application,Ljava/lang/String> >(line 751)
BB40
97   putfield v1 = v34:#TLS < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, sslProtocol, <Application,Ljava/lang/String> >(line 755)
BB41
100   putfield v1 = v5:#null < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, ciphers, <Application,Ljava/lang/String> >(line 761)
BB42
103   v35 = new <Application,[Ljava/lang/String>@200v4:#0 (line 762)
BB43
104   putfield v1 = v35 < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, ciphersarr, <Application,[Ljava/lang/String> >(line 762)
BB44
107   putfield v1 = v5:#null < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, keyAlias, <Application,Ljava/lang/String> >(line 775)
BB45
110   putfield v1 = v5:#null < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, keyPass, <Application,Ljava/lang/String> >(line 779)
BB46
113   v38 = invokestatic < Application, Ljava/lang/System, getProperty(Ljava/lang/String;)Ljava/lang/String; > v36:#javax.net.ssl.trustStore @219 exception:v37(line 783)
BB47
114   putfield v1 = v38 < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, truststoreFile, <Application,Ljava/lang/String> >(line 783)
BB48
117   v41 = invokestatic < Application, Ljava/lang/System, getProperty(Ljava/lang/String;)Ljava/lang/String; > v39:#javax.net.ssl.trustStorePassword @228 exception:v40(line 796)
BB49
118   putfield v1 = v41 < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, truststorePass, <Application,Ljava/lang/String> >(line 796)
BB50
121   v44 = invokestatic < Application, Ljava/lang/System, getProperty(Ljava/lang/String;)Ljava/lang/String; > v42:#javax.net.ssl.trustStoreType @237 exception:v43(line 803)
BB51
122   putfield v1 = v44 < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, truststoreType, <Application,Ljava/lang/String> >(line 803)
BB52
125   putfield v1 = v5:#null < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, truststoreProvider, <Application,Ljava/lang/String> >(line 809)
BB53
128   putfield v1 = v5:#null < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, truststoreAlgorithm, <Application,Ljava/lang/String> >(line 815)
BB54
131   putfield v1 = v5:#null < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, trustManagerClassName, <Application,Ljava/lang/String> >(line 821)
BB55
134   putfield v1 = v5:#null < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, crlFile, <Application,Ljava/lang/String> >(line 827)
BB56
137   putfield v1 = v5:#null < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, trustMaxCertLength, <Application,Ljava/lang/String> >(line 833)
BB57
140   putfield v1 = v5:#null < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, sessionCacheSize, <Application,Ljava/lang/String> >(line 839)
BB58
143   putfield v1 = v45:#86400 < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, sessionTimeout, <Application,Ljava/lang/String> >(line 843)
BB59
146   putfield v1 = v5:#null < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, allowUnsafeLegacyRenegotiation, <Application,Ljava/lang/String> >(line 847)
BB60
149   v46 = new <Application,[Ljava/lang/String>@286v4:#0 (line 856)
BB61
150   putfield v1 = v46 < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, sslEnabledProtocolsarr, <Application,[Ljava/lang/String> >(line 856)
BB62
151   return                                 (line 48)
BB63

**CGNode:** Node: < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, setMaxConnections(I)V > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, main([Ljava/lang/String;)V >:NEW <Application,Lorg/apache/tomcat/util/net/AprEndpoint>@0 in ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,[Ljava/lang/String>@6 in Everywhere} ]} ]
**IR:** < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, setMaxConnections(I)V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..2]
    -> BB2
    -> BB6
BB2[3..4]
    -> BB3
    -> BB6
BB3[5..8]
    -> BB5
    -> BB4
BB4[9..12]
    -> BB5
    -> BB6
BB5[13..13]
    -> BB6
BB6[-1..-2]
Instructions:
BB0
BB1
2   putfield v1 = v2 < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, maxConnections, <Primordial,I> >(line 164)
BB2
4   v4 = getfield < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, connectionLimitLatch, <Application,Lorg/apache/tomcat/util/threads/LimitLatch> > v1(line 165)
BB3
8   conditional branch(eq) v4,v5:#null       (line 166)
BB4
11   v6 = conversion(J) v2                   (line 168)
12   invokevirtual < Application, Lorg/apache/tomcat/util/threads/LimitLatch, setLimit(J)V > v4,v6 @17 exception:v7(line 168)
BB5
13   return                                  (line 170)
BB6

**CGNode:** Node: < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, getAcceptorThreadCount()I > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, main([Ljava/lang/String;)V >:NEW <Application,Lorg/apache/tomcat/util/net/AprEndpoint>@0 in ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,[Ljava/lang/String>@6 in Everywhere} ]} ]
**IR:** < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, getAcceptorThreadCount()I >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..1]
    -> BB2
    -> BB3
BB2[2..2]
    -> BB3
BB3[-1..-2]
Instructions:
BB0
BB1
1   v3 = getfield < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, acceptorThreadCount, <Primordial,I> > v1(line 149)
BB2
2   return v3                                (line 149)
BB3

**CGNode:** Node: < Application, Lorg/apache/tomcat/util/net/AprEndpoint, createAcceptor()Lorg/apache/tomcat/util/net/AbstractEndpoint$Acceptor; > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, main([Ljava/lang/String;)V >:NEW <Application,Lorg/apache/tomcat/util/net/AprEndpoint>@0 in ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,[Ljava/lang/String>@6 in Everywhere} ]} ]
**IR:** < Application, Lorg/apache/tomcat/util/net/AprEndpoint, createAcceptor()Lorg/apache/tomcat/util/net/AbstractEndpoint$Acceptor; >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..0]
    -> BB2
    -> BB4
BB2[1..3]
    -> BB3
    -> BB4
BB3[4..4]
    -> BB4
BB4[-1..-2]
Instructions:
BB0
BB1
0   v3 = new <Application,Lorg/apache/tomcat/util/net/AprEndpoint$Acceptor>@0(line 753)
BB2
3   invokespecial < Application, Lorg/apache/tomcat/util/net/AprEndpoint$Acceptor, <init>(Lorg/apache/tomcat/util/net/AprEndpoint;)V > v3,v1 @5 exception:v4(line 753)
BB3
4   return v3                                (line 753)
BB4

**CGNode:** Node: < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, getName()Ljava/lang/String; > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, main([Ljava/lang/String;)V >:NEW <Application,Lorg/apache/tomcat/util/net/AprEndpoint>@0 in ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,[Ljava/lang/String>@6 in Everywhere} ]} ]
**IR:** < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, getName()Ljava/lang/String; >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..1]
    -> BB2
    -> BB3
BB2[2..2]
    -> BB3
BB3[-1..-2]
Instructions:
BB0
BB1
1   v3 = getfield < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, name, <Application,Ljava/lang/String> > v1(line 326)
BB2
2   return v3                                (line 326)
BB3

**CGNode:** Node: < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, getAcceptorThreadPriority()I > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, main([Ljava/lang/String;)V >:NEW <Application,Lorg/apache/tomcat/util/net/AprEndpoint>@0 in ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,[Ljava/lang/String>@6 in Everywhere} ]} ]
**IR:** < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, getAcceptorThreadPriority()I >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..1]
    -> BB2
    -> BB3
BB2[2..2]
    -> BB3
BB3[-1..-2]
Instructions:
BB0
BB1
1   v3 = getfield < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, acceptorThreadPriority, <Primordial,I> > v1(line 159)
BB2
2   return v3                                (line 159)
BB3

**CGNode:** Node: < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, getDaemon()Z > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, main([Ljava/lang/String;)V >:NEW <Application,Lorg/apache/tomcat/util/net/AprEndpoint>@0 in ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,[Ljava/lang/String>@6 in Everywhere} ]} ]
**IR:** < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, getDaemon()Z >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..1]
    -> BB2
    -> BB3
BB2[2..2]
    -> BB3
BB3[-1..-2]
Instructions:
BB0
BB1
1   v3 = getfield < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, daemon, <Primordial,Z> > v1(line 335)
BB2
2   return v3                                (line 335)
BB3

**CGNode:** Node: < Application, Lorg/apache/tomcat/util/res/StringManager, getManager(Ljava/lang/String;Ljava/util/Locale;)Lorg/apache/tomcat/util/res/StringManager; > Context: ReceiverStringContext: [ [<Primordial,Ljava/lang/String>] ]
**IR:** < Application, Lorg/apache/tomcat/util/res/StringManager, getManager(Ljava/lang/String;Ljava/util/Locale;)Lorg/apache/tomcat/util/res/StringManager; >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..2]
    -> BB2
    -> BB16
BB2[3..3]
    -> BB3
    -> BB16
BB3[4..7]
    -> BB8
    -> BB4
BB4[8..8]
    -> BB5
    -> BB16
BB5[9..10]
    -> BB6
    -> BB16
BB6[11..15]
    -> BB7
    -> BB16
BB7[16..16]
    -> BB8
BB8[17..19]
    -> BB9
    -> BB16
BB9[20..20]
    -> BB10
    -> BB16
BB10[21..24]
    -> BB15
    -> BB11
BB11[25..25]
    -> BB12
    -> BB16
BB12[26..29]
    -> BB13
    -> BB16
BB13[30..34]
    -> BB14
    -> BB16
BB14[35..35]
    -> BB15
BB15[36..37]
    -> BB16
BB16[-1..-2]
Instructions:
BB0
BB1
0   v4 = getstatic < Application, Lorg/apache/tomcat/util/res/StringManager, managers, <Application,Ljava/util/Map> >(line 193)
2   v6 = invokeinterface < Application, Ljava/util/Map, get(Ljava/lang/Object;)Ljava/lang/Object; > v4,v1 @4 exception:v5(line 193)
BB2
3   v7 = checkcast <Application,Ljava/util/Map>v6(line 193)
BB3
7   conditional branch(ne) v7,v8:#null       (line 194)
BB4
8   v9 = new <Application,Ljava/util/Hashtable>@17(line 195)
BB5
10   invokespecial < Application, Ljava/util/Hashtable, <init>()V > v9 @21 exception:v10(line 195)
BB6
12   v11 = getstatic < Application, Lorg/apache/tomcat/util/res/StringManager, managers, <Application,Ljava/util/Map> >(line 196)
15   v13 = invokeinterface < Application, Ljava/util/Map, put(Ljava/lang/Object;Ljava/lang/Object;)Ljava/lang/Object; > v11,v1,v9 @30 exception:v12(line 196)
BB7
BB8
           v14 = phi  v7,v9
19   v16 = invokeinterface < Application, Ljava/util/Map, get(Ljava/lang/Object;)Ljava/lang/Object; > v14,v2 @38 exception:v15(line 199)
BB9
20   v17 = checkcast <Application,Lorg/apache/tomcat/util/res/StringManager>v16(line 199)
BB10
24   conditional branch(ne) v17,v8:#null     (line 200)
BB11
25   v18 = new <Application,Lorg/apache/tomcat/util/res/StringManager>@51(line 201)
BB12
29   invokespecial < Application, Lorg/apache/tomcat/util/res/StringManager, <init>(Ljava/lang/String;Ljava/util/Locale;)V > v18,v1,v2 @57 exception:v19(line 201)
BB13
34   v21 = invokeinterface < Application, Ljava/util/Map, put(Ljava/lang/Object;Ljava/lang/Object;)Ljava/lang/Object; > v14,v2,v18 @64 exception:v20(line 202)
BB14
BB15
           v22 = phi  v17,v18
37   return v22                              (line 204)
BB16

**CGNode:** Node: < Application, Lorg/apache/juli/logging/LogFactory, getFactory()Lorg/apache/juli/logging/LogFactory; > Context: ReceiverStringContext: [ [<Primordial,Ljava/lang/Class>] ]
**IR:** < Application, Lorg/apache/juli/logging/LogFactory, getFactory()Lorg/apache/juli/logging/LogFactory; >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..1]
    -> BB2
BB2[-1..-2]
Instructions:
BB0
BB1
0   v2 = getstatic < Application, Lorg/apache/juli/logging/LogFactory, singleton, <Application,Lorg/apache/juli/logging/LogFactory> >(line 150)
1   return v2                                (line 150)
BB2

**CGNode:** Node: < Application, Lorg/apache/juli/logging/LogFactory, <init>()V > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/juli/logging/LogFactory, <clinit>()V >:NEW <Application,Lorg/apache/juli/logging/LogFactory>@0 in Everywhere} ]
**IR:** < Application, Lorg/apache/juli/logging/LogFactory, <init>()V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..1]
    -> BB2
    -> BB3
BB2[2..2]
    -> BB3
BB3[-1..-2]
Instructions:
BB0
BB1
1   invokespecial < Application, Ljava/lang/Object, <init>()V > v1 @1 exception:v3(line 72)
BB2
2   return                                   (line 73)
BB3

**CGNode:** Node: < Application, Lorg/apache/catalina/tribes/transport/bio/util/SingleRemoveSynchronizedAddLock, <init>()V > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/transport/bio/util/FastQueue, <init>()V >:NEW <Application,Lorg/apache/catalina/tribes/transport/bio/util/SingleRemoveSynchronizedAddLock>@49 in ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/group/interceptors/MessageDispatchInterceptor, <init>()V >:NEW <Application,Lorg/apache/catalina/tribes/transport/bio/util/FastQueue>@12 in ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,Lorg/apache/catalina/tribes/group/interceptors/MessageDispatchInterceptor>@11 in Everywhere} ]} ]} ]
**IR:** < Application, Lorg/apache/catalina/tribes/transport/bio/util/SingleRemoveSynchronizedAddLock, <init>()V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..1]
    -> BB2
    -> BB10
BB2[2..4]
    -> BB3
    -> BB10
BB3[5..7]
    -> BB4
    -> BB10
BB4[8..10]
    -> BB5
    -> BB10
BB5[11..13]
    -> BB6
    -> BB10
BB6[14..16]
    -> BB7
    -> BB10
BB7[17..19]
    -> BB8
    -> BB10
BB8[20..22]
    -> BB9
    -> BB10
BB9[23..23]
    -> BB10
BB10[-1..-2]
Instructions:
BB0
BB1
1   invokespecial < Application, Ljava/lang/Object, <init>()V > v1 @1 exception:v3(line 54)
BB2
4   putfield v1 = v4:#10000 < Application, Lorg/apache/catalina/tribes/transport/bio/util/SingleRemoveSynchronizedAddLock, addWaitTimeout, <Primordial,J> >(line 69)
BB3
7   putfield v1 = v5:#30000 < Application, Lorg/apache/catalina/tribes/transport/bio/util/SingleRemoveSynchronizedAddLock, removeWaitTimeout, <Primordial,J> >(line 78)
BB4
10   putfield v1 = v6:#null < Application, Lorg/apache/catalina/tribes/transport/bio/util/SingleRemoveSynchronizedAddLock, remover, <Application,Ljava/lang/Thread> >(line 87)
BB5
13   putfield v1 = v7:#0 < Application, Lorg/apache/catalina/tribes/transport/bio/util/SingleRemoveSynchronizedAddLock, addLocked, <Primordial,Z> >(line 92)
BB6
16   putfield v1 = v7:#0 < Application, Lorg/apache/catalina/tribes/transport/bio/util/SingleRemoveSynchronizedAddLock, removeLocked, <Primordial,Z> >(line 97)
BB7
19   putfield v1 = v8:#1 < Application, Lorg/apache/catalina/tribes/transport/bio/util/SingleRemoveSynchronizedAddLock, removeEnabled, <Primordial,Z> >(line 103)
BB8
22   putfield v1 = v7:#0 < Application, Lorg/apache/catalina/tribes/transport/bio/util/SingleRemoveSynchronizedAddLock, dataAvailable, <Primordial,Z> >(line 110)
BB9
23   return                                  (line 56)
BB10

**CGNode:** Node: < Application, Lorg/apache/catalina/tribes/transport/bio/util/SingleRemoveSynchronizedAddLock, setAddWaitTimeout(J)V > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/transport/bio/util/FastQueue, <init>()V >:NEW <Application,Lorg/apache/catalina/tribes/transport/bio/util/SingleRemoveSynchronizedAddLock>@49 in ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/group/interceptors/MessageDispatchInterceptor, <init>()V >:NEW <Application,Lorg/apache/catalina/tribes/transport/bio/util/FastQueue>@12 in ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,Lorg/apache/catalina/tribes/group/interceptors/MessageDispatchInterceptor>@11 in Everywhere} ]} ]} ]
**IR:** < Application, Lorg/apache/catalina/tribes/transport/bio/util/SingleRemoveSynchronizedAddLock, setAddWaitTimeout(J)V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..2]
    -> BB2
    -> BB3
BB2[3..3]
    -> BB3
BB3[-1..-2]
Instructions:
BB0
BB1
2   putfield v1 = v2 < Application, Lorg/apache/catalina/tribes/transport/bio/util/SingleRemoveSynchronizedAddLock, addWaitTimeout, <Primordial,J> >(line 123)
BB2
3   return                                   (line 124)
BB3

**CGNode:** Node: < Application, Lorg/apache/catalina/tribes/transport/bio/util/SingleRemoveSynchronizedAddLock, setRemoveWaitTimeout(J)V > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/transport/bio/util/FastQueue, <init>()V >:NEW <Application,Lorg/apache/catalina/tribes/transport/bio/util/SingleRemoveSynchronizedAddLock>@49 in ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/group/interceptors/MessageDispatchInterceptor, <init>()V >:NEW <Application,Lorg/apache/catalina/tribes/transport/bio/util/FastQueue>@12 in ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,Lorg/apache/catalina/tribes/group/interceptors/MessageDispatchInterceptor>@11 in Everywhere} ]} ]} ]
**IR:** < Application, Lorg/apache/catalina/tribes/transport/bio/util/SingleRemoveSynchronizedAddLock, setRemoveWaitTimeout(J)V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..2]
    -> BB2
    -> BB3
BB2[3..3]
    -> BB3
BB3[-1..-2]
Instructions:
BB0
BB1
2   putfield v1 = v2 < Application, Lorg/apache/catalina/tribes/transport/bio/util/SingleRemoveSynchronizedAddLock, removeWaitTimeout, <Primordial,J> >(line 137)
BB2
3   return                                   (line 138)
BB3

**CGNode:** Node: < Application, Lorg/apache/catalina/tribes/group/ChannelInterceptorBase, setOptionFlag(I)V > Context: ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,Lorg/apache/catalina/tribes/group/interceptors/MessageDispatchInterceptor>@11 in Everywhere} ]
**IR:** < Application, Lorg/apache/catalina/tribes/group/ChannelInterceptorBase, setOptionFlag(I)V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..2]
    -> BB2
    -> BB3
BB2[3..3]
    -> BB3
BB3[-1..-2]
Instructions:
BB0
BB1
2   putfield v1 = v2 < Application, Lorg/apache/catalina/tribes/group/ChannelInterceptorBase, optionFlag, <Primordial,I> >(line 63)
BB2
3   return                                   (line 64)
BB3

**CGNode:** Node: < Application, Lorg/apache/catalina/tribes/transport/bio/util/FastQueue, remove()Lorg/apache/catalina/tribes/transport/bio/util/LinkObject; > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/group/interceptors/MessageDispatchInterceptor, <init>()V >:NEW <Application,Lorg/apache/catalina/tribes/transport/bio/util/FastQueue>@12 in ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,Lorg/apache/catalina/tribes/group/interceptors/MessageDispatchInterceptor>@11 in Everywhere} ]} ]
**IR:** < Application, Lorg/apache/catalina/tribes/transport/bio/util/FastQueue, remove()Lorg/apache/catalina/tribes/transport/bio/util/LinkObject; >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..1]
    -> BB2
    -> BB49
BB2[2..3]
    -> BB7
    -> BB3
BB3[4..5]
    -> BB4
    -> BB49
BB4[6..7]
    -> BB6
    -> BB5
BB5[8..10]
    -> BB6
    -> BB49
BB6[11..12]
    -> BB49
BB7[13..14]
    -> BB8
    -> BB49
BB8[15..15]
    -> BB9
    -> BB49
BB9[16..19]
    -> BB22
    -> BB10
BB10[20..21]
    -> BB11
    -> BB43
BB11[22..23]
    -> BB16
    -> BB12
BB12[24..25]
    -> BB13
    -> BB43
BB13[26..27]
    -> BB19
    -> BB14
BB14[28..30]
    -> BB15
    -> BB43
BB15[31..31]
    -> BB19
BB16[32..33]
    -> BB17
    -> BB43
BB17[34..35]
    -> BB19
    -> BB18
BB18[36..38]
    -> BB19
    -> BB43
BB19[39..40]
    -> BB20
    -> BB49
BB20[41..41]
    -> BB21
    -> BB49
BB21[42..43]
    -> BB49
BB22[44..45]
    -> BB23
    -> BB43
BB23[46..47]
    -> BB30
    -> BB24
BB24[48..49]
    -> BB25
    -> BB43
BB25[50..52]
    -> BB26
    -> BB43
BB26[53..54]
    -> BB27
    -> BB43
BB27[55..55]
    -> BB28
    -> BB43
BB28[56..56]
    -> BB29
    -> BB43
BB29[57..57]
    -> BB30
    -> BB43
BB30[58..59]
    -> BB31
    -> BB43
BB31[60..65]
    -> BB32
    -> BB43
BB32[66..66]
    -> BB33
    -> BB43
BB33[67..69]
    -> BB34
    -> BB43
BB34[70..71]
    -> BB35
    -> BB43
BB35[72..73]
    -> BB46
    -> BB36
BB36[74..75]
    -> BB37
    -> BB43
BB37[76..78]
    -> BB38
    -> BB43
BB38[79..80]
    -> BB39
    -> BB43
BB39[81..81]
    -> BB40
    -> BB43
BB40[82..82]
    -> BB41
    -> BB43
BB41[83..83]
    -> BB42
    -> BB43
BB42[84..84]
    -> BB46
BB43[85..87]
    -> BB44
    -> BB49
BB44[88..88]
    -> BB45
    -> BB49
BB45[89..90]
    -> BB49
BB46[91..92]
    -> BB47
    -> BB49
BB47[93..93]
    -> BB48
    -> BB49
BB48[94..95]
    -> BB49
BB49[-1..-2]
Instructions:
BB0
BB1
1   v3 = getfield < Application, Lorg/apache/catalina/tribes/transport/bio/util/FastQueue, enabled, <Primordial,Z> > v1(line 253)
BB2
3   conditional branch(ne) v3,v4:#0          (line 253)
BB3
4   v56 = getstatic < Application, Lorg/apache/catalina/tribes/transport/bio/util/FastQueue, log, <Application,Lorg/apache/juli/logging/Log> >(line 254)
5   v58 = invokeinterface < Application, Lorg/apache/juli/logging/Log, isInfoEnabled()Z > v56 @10 exception:v57(line 254)
BB4
7   conditional branch(eq) v58,v4:#0         (line 254)
BB5
8   v59 = getstatic < Application, Lorg/apache/catalina/tribes/transport/bio/util/FastQueue, log, <Application,Lorg/apache/juli/logging/Log> >(line 255)
10   invokeinterface < Application, Lorg/apache/juli/logging/Log, info(Ljava/lang/Object;)V > v59,v43:#FastQueue.remove: queue disabled, remove aborted @23 exception:v60(line 255)
BB6
12   return v22:#null                        (line 256)
BB7
14   v5 = getfield < Application, Lorg/apache/catalina/tribes/transport/bio/util/FastQueue, lock, <Application,Lorg/apache/catalina/tribes/transport/bio/util/SingleRemoveSynchronizedAddLock> > v1(line 259)
BB8
15   v7 = invokevirtual < Application, Lorg/apache/catalina/tribes/transport/bio/util/SingleRemoveSynchronizedAddLock, lockRemove()Z > v5 @34 exception:v6(line 259)
BB9
19   conditional branch(ne) v7,v4:#0         (line 262)
BB10
21   v38 = getfield < Application, Lorg/apache/catalina/tribes/transport/bio/util/FastQueue, enabled, <Primordial,Z> > v1(line 263)
BB11
23   conditional branch(eq) v38,v4:#0        (line 263)
BB12
24   v45 = getstatic < Application, Lorg/apache/catalina/tribes/transport/bio/util/FastQueue, log, <Application,Lorg/apache/juli/logging/Log> >(line 264)
25   v47 = invokeinterface < Application, Lorg/apache/juli/logging/Log, isInfoEnabled()Z > v45 @52 exception:v46(line 264)
BB13
27   conditional branch(eq) v47,v4:#0        (line 264)
BB14
28   v48 = getstatic < Application, Lorg/apache/catalina/tribes/transport/bio/util/FastQueue, log, <Application,Lorg/apache/juli/logging/Log> >(line 265)
30   invokeinterface < Application, Lorg/apache/juli/logging/Log, info(Ljava/lang/Object;)V > v48,v49:#FastQueue.remove: Remove aborted although queue enabled @65 exception:v50(line 265)
BB15
31   goto                                    (line 265)
BB16
32   v39 = getstatic < Application, Lorg/apache/catalina/tribes/transport/bio/util/FastQueue, log, <Application,Lorg/apache/juli/logging/Log> >(line 267)
33   v41 = invokeinterface < Application, Lorg/apache/juli/logging/Log, isInfoEnabled()Z > v39 @76 exception:v40(line 267)
BB17
35   conditional branch(eq) v41,v4:#0        (line 267)
BB18
36   v42 = getstatic < Application, Lorg/apache/catalina/tribes/transport/bio/util/FastQueue, log, <Application,Lorg/apache/juli/logging/Log> >(line 268)
38   invokeinterface < Application, Lorg/apache/juli/logging/Log, info(Ljava/lang/Object;)V > v42,v43:#FastQueue.remove: queue disabled, remove aborted @89 exception:v44(line 268)
BB19
40   v54 = getfield < Application, Lorg/apache/catalina/tribes/transport/bio/util/FastQueue, lock, <Application,Lorg/apache/catalina/tribes/transport/bio/util/SingleRemoveSynchronizedAddLock> > v1(line 287)
BB20
41   invokevirtual < Application, Lorg/apache/catalina/tribes/transport/bio/util/SingleRemoveSynchronizedAddLock, unlockRemove()V > v54 @98 exception:v55(line 287)
BB21
43   return v22:#null                        (line 270)
BB22
44   v8 = getstatic < Application, Lorg/apache/catalina/tribes/transport/bio/util/FastQueue, log, <Application,Lorg/apache/juli/logging/Log> >(line 273)
45   v10 = invokeinterface < Application, Lorg/apache/juli/logging/Log, isTraceEnabled()Z > v8 @106 exception:v9(line 273)
BB23
47   conditional branch(eq) v10,v4:#0        (line 273)
BB24
48   v11 = getstatic < Application, Lorg/apache/catalina/tribes/transport/bio/util/FastQueue, log, <Application,Lorg/apache/juli/logging/Log> >(line 274)
49   v12 = new <Application,Ljava/lang/StringBuilder>@117(line 274)
BB25
52   invokespecial < Application, Ljava/lang/StringBuilder, <init>(Ljava/lang/String;)V > v12,v13:#FastQueue.remove: remove starting with size  @123 exception:v14(line 274)
BB26
54   v15 = getfield < Application, Lorg/apache/catalina/tribes/transport/bio/util/FastQueue, size, <Primordial,I> > v1(line 274)
BB27
55   v17 = invokevirtual < Application, Ljava/lang/StringBuilder, append(I)Ljava/lang/StringBuilder; > v12,v15 @130 exception:v16(line 274)
BB28
56   v19 = invokevirtual < Application, Ljava/lang/StringBuilder, toString()Ljava/lang/String; > v17 @133 exception:v18(line 274)
BB29
57   invokeinterface < Application, Lorg/apache/juli/logging/Log, trace(Ljava/lang/Object;)V > v11,v19 @136 exception:v20(line 274)
BB30
59   v21 = getfield < Application, Lorg/apache/catalina/tribes/transport/bio/util/FastQueue, first, <Application,Lorg/apache/catalina/tribes/transport/bio/util/LinkObject> > v1(line 277)
BB31
65   putfield v1 = v22:#null < Application, Lorg/apache/catalina/tribes/transport/bio/util/FastQueue, last, <Application,Lorg/apache/catalina/tribes/transport/bio/util/LinkObject> >(line 279)
BB32
66   putfield v1 = v22:#null < Application, Lorg/apache/catalina/tribes/transport/bio/util/FastQueue, first, <Application,Lorg/apache/catalina/tribes/transport/bio/util/LinkObject> >(line 279)
BB33
69   putfield v1 = v4:#0 < Application, Lorg/apache/catalina/tribes/transport/bio/util/FastQueue, size, <Primordial,I> >(line 280)
BB34
70   v23 = getstatic < Application, Lorg/apache/catalina/tribes/transport/bio/util/FastQueue, log, <Application,Lorg/apache/juli/logging/Log> >(line 282)
71   v25 = invokeinterface < Application, Lorg/apache/juli/logging/Log, isTraceEnabled()Z > v23 @164 exception:v24(line 282)
BB35
73   conditional branch(eq) v25,v4:#0        (line 282)
BB36
74   v26 = getstatic < Application, Lorg/apache/catalina/tribes/transport/bio/util/FastQueue, log, <Application,Lorg/apache/juli/logging/Log> >(line 283)
75   v27 = new <Application,Ljava/lang/StringBuilder>@175(line 283)
BB37
78   invokespecial < Application, Ljava/lang/StringBuilder, <init>(Ljava/lang/String;)V > v27,v28:#FastQueue.remove: remove ending with size  @181 exception:v29(line 283)
BB38
80   v30 = getfield < Application, Lorg/apache/catalina/tribes/transport/bio/util/FastQueue, size, <Primordial,I> > v1(line 283)
BB39
81   v32 = invokevirtual < Application, Ljava/lang/StringBuilder, append(I)Ljava/lang/StringBuilder; > v27,v30 @188 exception:v31(line 283)
BB40
82   v34 = invokevirtual < Application, Ljava/lang/StringBuilder, toString()Ljava/lang/String; > v32 @191 exception:v33(line 283)
BB41
83   invokeinterface < Application, Lorg/apache/juli/logging/Log, trace(Ljava/lang/Object;)V > v26,v34 @194 exception:v35(line 283)
BB42
84   goto                                    (line 283)
BB43<Handler>
           v51 = getCaughtException 
87   v52 = getfield < Application, Lorg/apache/catalina/tribes/transport/bio/util/FastQueue, lock, <Application,Lorg/apache/catalina/tribes/transport/bio/util/SingleRemoveSynchronizedAddLock> > v1(line 287)
BB44
88   invokevirtual < Application, Lorg/apache/catalina/tribes/transport/bio/util/SingleRemoveSynchronizedAddLock, unlockRemove()V > v52 @207 exception:v53(line 287)
BB45
90   throw v51                               (line 288)
BB46
92   v36 = getfield < Application, Lorg/apache/catalina/tribes/transport/bio/util/FastQueue, lock, <Application,Lorg/apache/catalina/tribes/transport/bio/util/SingleRemoveSynchronizedAddLock> > v1(line 287)
BB47
93   invokevirtual < Application, Lorg/apache/catalina/tribes/transport/bio/util/SingleRemoveSynchronizedAddLock, unlockRemove()V > v36 @216 exception:v37(line 287)
BB48
95   return v21                              (line 289)
BB49

**CGNode:** Node: < Application, Lorg/apache/catalina/tribes/group/ChannelInterceptorBase, sendMessage([Lorg/apache/catalina/tribes/Member;Lorg/apache/catalina/tribes/ChannelMessage;Lorg/apache/catalina/tribes/group/InterceptorPayload;)V > Context: ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,Lorg/apache/catalina/tribes/group/interceptors/MessageDispatchInterceptor>@11 in Everywhere} ]
**IR:** < Application, Lorg/apache/catalina/tribes/group/ChannelInterceptorBase, sendMessage([Lorg/apache/catalina/tribes/Member;Lorg/apache/catalina/tribes/ChannelMessage;Lorg/apache/catalina/tribes/group/InterceptorPayload;)V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..1]
    -> BB2
    -> BB6
BB2[2..3]
    -> BB5
    -> BB3
BB3[4..5]
    -> BB4
    -> BB6
BB4[6..9]
    -> BB5
    -> BB6
BB5[10..10]
    -> BB6
BB6[-1..-2]
Instructions:
BB0
BB1
1   v7 = invokevirtual < Application, Lorg/apache/catalina/tribes/group/ChannelInterceptorBase, getNext()Lorg/apache/catalina/tribes/ChannelInterceptor; > v1 @1 exception:v6(line 79)
BB2
3   conditional branch(eq) v7,v8:#null       (line 79)
BB3
5   v10 = invokevirtual < Application, Lorg/apache/catalina/tribes/group/ChannelInterceptorBase, getNext()Lorg/apache/catalina/tribes/ChannelInterceptor; > v1 @8 exception:v9(line 79)
BB4
9   invokeinterface < Application, Lorg/apache/catalina/tribes/ChannelInterceptor, sendMessage([Lorg/apache/catalina/tribes/Member;Lorg/apache/catalina/tribes/ChannelMessage;Lorg/apache/catalina/tribes/group/InterceptorPayload;)V > v10,v2,v3,v4 @14 exception:v11(line 79)
BB5
10   return                                  (line 80)
BB6

**CGNode:** Node: < Application, Lorg/apache/catalina/tribes/UniqueId, <init>([B)V > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/group/interceptors/MessageDispatchInterceptor, sendAsyncData(Lorg/apache/catalina/tribes/transport/bio/util/LinkObject;)Lorg/apache/catalina/tribes/transport/bio/util/LinkObject; >:NEW <Application,Lorg/apache/catalina/tribes/UniqueId>@28 in ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,Lorg/apache/catalina/tribes/group/interceptors/MessageDispatchInterceptor>@11 in Everywhere} ]} ]
**IR:** < Application, Lorg/apache/catalina/tribes/UniqueId, <init>([B)V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..1]
    -> BB2
    -> BB4
BB2[2..4]
    -> BB3
    -> BB4
BB3[5..5]
    -> BB4
BB4[-1..-2]
Instructions:
BB0
BB1
1   invokespecial < Application, Ljava/lang/Object, <init>()V > v1 @1 exception:v4(line 39)
BB2
4   putfield v1 = v2 < Application, Lorg/apache/catalina/tribes/UniqueId, id, <Primordial,[B> >(line 40)
BB3
5   return                                   (line 41)
BB4

**CGNode:** Node: < Application, Lorg/apache/catalina/tribes/ChannelException, <clinit>()V > Context: Everywhere
**IR:** < Application, Lorg/apache/catalina/tribes/ChannelException, <clinit>()V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..1]
    -> BB2
    -> BB3
BB2[2..3]
    -> BB3
BB3[-1..-2]
Instructions:
BB0
BB1
1   v3 = new <Application,[Lorg/apache/catalina/tribes/ChannelException$FaultyMember>@1v2:#0 (line 38)
BB2
2   putstatic v3 < Application, Lorg/apache/catalina/tribes/ChannelException, EMPTY_LIST, <Application,[Lorg/apache/catalina/tribes/ChannelException$FaultyMember> >(line 38)
3   return                                   (line 33)
BB3

**CGNode:** Node: < Application, Lorg/apache/catalina/tribes/ChannelException, <init>(Ljava/lang/Throwable;)V > Context: ReceiverStringContext: [ [<Application,Lorg/apache/catalina/tribes/ChannelException>] ]
**IR:** < Application, Lorg/apache/catalina/tribes/ChannelException, <init>(Ljava/lang/Throwable;)V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..2]
    -> BB2
    -> BB4
BB2[3..5]
    -> BB3
    -> BB4
BB3[6..6]
    -> BB4
BB4[-1..-2]
Instructions:
BB0
BB1
2   invokespecial < Application, Ljava/lang/Exception, <init>(Ljava/lang/Throwable;)V > v1,v2 @2 exception:v4(line 76)
BB2
5   putfield v1 = v5:#null < Application, Lorg/apache/catalina/tribes/ChannelException, faultyMembers, <Application,Ljava/util/ArrayList> >(line 42)
BB3
6   return                                   (line 77)
BB4

**CGNode:** Node: < Application, Lorg/apache/catalina/tribes/UniqueId, <init>([B)V > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/group/interceptors/MessageDispatchInterceptor, sendAsyncData(Lorg/apache/catalina/tribes/transport/bio/util/LinkObject;)Lorg/apache/catalina/tribes/transport/bio/util/LinkObject; >:NEW <Application,Lorg/apache/catalina/tribes/UniqueId>@136 in ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,Lorg/apache/catalina/tribes/group/interceptors/MessageDispatchInterceptor>@11 in Everywhere} ]} ]
**IR:** < Application, Lorg/apache/catalina/tribes/UniqueId, <init>([B)V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..1]
    -> BB2
    -> BB4
BB2[2..4]
    -> BB3
    -> BB4
BB3[5..5]
    -> BB4
BB4[-1..-2]
Instructions:
BB0
BB1
1   invokespecial < Application, Ljava/lang/Object, <init>()V > v1 @1 exception:v4(line 39)
BB2
4   putfield v1 = v2 < Application, Lorg/apache/catalina/tribes/UniqueId, id, <Primordial,[B> >(line 40)
BB3
5   return                                   (line 41)
BB4

**CGNode:** Node: < Application, Lorg/apache/catalina/tribes/group/interceptors/MessageDispatchInterceptor, addAndGetCurrentSize(J)J > Context: ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,Lorg/apache/catalina/tribes/group/interceptors/MessageDispatchInterceptor>@11 in Everywhere} ]
**IR:** < Application, Lorg/apache/catalina/tribes/group/interceptors/MessageDispatchInterceptor, addAndGetCurrentSize(J)J >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..3]
    -> BB2
    -> BB9
BB2[4..6]
    -> BB3
    -> BB7
BB3[7..9]
    -> BB4
    -> BB7
BB4[10..11]
    -> BB5
    -> BB7
BB5[12..13]
    -> BB6
    -> BB7
BB6[14..14]
    -> BB9
BB7[15..16]
    -> BB8
    -> BB7
BB8[17..17]
    -> BB9
BB9[-1..-2]
Instructions:
BB0
BB1
3   monitorenter v1                          (line 136)
BB2
6   v4 = getfield < Application, Lorg/apache/catalina/tribes/group/interceptors/MessageDispatchInterceptor, currentSize, <Primordial,J> > v1(line 137)
BB3
8   v5 = binaryop(add) v4 , v2               (line 137)
9   putfield v1 = v5 < Application, Lorg/apache/catalina/tribes/group/interceptors/MessageDispatchInterceptor, currentSize, <Primordial,J> >(line 137)
BB4
11   v6 = getfield < Application, Lorg/apache/catalina/tribes/group/interceptors/MessageDispatchInterceptor, currentSize, <Primordial,J> > v1(line 138)
BB5
13   monitorexit v1                          (line 138)
BB6
14   return v6                               (line 138)
BB7<Handler>
           v7 = getCaughtException 
16   monitorexit v1                          (line 136)
BB8
17   throw v7                                (line 136)
BB9

**CGNode:** Node: < Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, access$0(JDILjava/text/DecimalFormat;Ljava/math/BigDecimal;)V > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, main([Ljava/lang/String;)V >:NEW <Application,Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive$1>@68 in ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,[Ljava/lang/String>@1 in Everywhere} ]} ]
**IR:** < Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, access$0(JDILjava/text/DecimalFormat;Ljava/math/BigDecimal;)V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..5]
    -> BB2
    -> BB3
BB2[6..6]
    -> BB3
BB3[-1..-2]
Instructions:
BB0
BB1
5   invokestatic < Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, printStats(JDILjava/text/DecimalFormat;Ljava/math/BigDecimal;)V > v1,v2,v3,v4,v5 @8 exception:v7(line 87)
BB2
6   return                                   (line 87)
BB3

**CGNode:** Node: < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, toInt([BI)I > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/io/XByteBuffer, expand(I)V >:NEW <Primordial,[B>@11 in ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, main([Ljava/lang/String;)V >:NEW <Application,Lorg/apache/catalina/tribes/io/XByteBuffer>@19 in ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,[Ljava/lang/String>@1 in Everywhere} ]} ]} ]
**IR:** < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, toInt([BI)I >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..4]
    -> BB2
    -> BB6
BB2[5..11]
    -> BB3
    -> BB6
BB3[12..21]
    -> BB4
    -> BB6
BB4[22..31]
    -> BB5
    -> BB6
BB5[32..37]
    -> BB6
BB6[-1..-2]
Instructions:
BB0
BB1
3   v5 = binaryop(add) v2 , v4:#3            (line 396)
4   v6 = arrayload v1[v5]                    (line 396)
BB2
6   v8 = binaryop(and) v6 , v7:#255          (line 396)
10   v10 = binaryop(add) v2 , v9:#2          (line 397)
11   v11 = arrayload v1[v10]                 (line 397)
BB3
13   v12 = binaryop(and) v11 , v7:#255       (line 397)
15   v14 = binaryop(SHL) v12 , v13:#8        (line 397)
16   v15 = binaryop(add) v8 , v14            (line 396)
20   v17 = binaryop(add) v2 , v16:#1         (line 398)
21   v18 = arrayload v1[v17]                 (line 398)
BB4
23   v19 = binaryop(and) v18 , v7:#255       (line 398)
25   v21 = binaryop(SHL) v19 , v20:#16       (line 398)
26   v22 = binaryop(add) v15 , v21           (line 396)
30   v24 = binaryop(add) v2 , v23:#0         (line 399)
31   v25 = arrayload v1[v24]                 (line 399)
BB5
33   v26 = binaryop(and) v25 , v7:#255       (line 399)
35   v28 = binaryop(SHL) v26 , v27:#24       (line 399)
36   v29 = binaryop(add) v22 , v28           (line 396)
37   return v29                              (line 396)
BB6

**CGNode:** Node: < Application, Lorg/apache/catalina/tribes/io/BufferPool, getBufferPool()Lorg/apache/catalina/tribes/io/BufferPool; > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, main([Ljava/lang/String;)V >:NEW <Application,Lorg/apache/catalina/tribes/io/XByteBuffer>@19 in ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,[Ljava/lang/String>@1 in Everywhere} ]} ]
**IR:** < Application, Lorg/apache/catalina/tribes/io/BufferPool, getBufferPool()Lorg/apache/catalina/tribes/io/BufferPool; >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..2]
    -> BB36
    -> BB2
BB2[3..3]
    -> BB3
    -> BB37
BB3[4..6]
    -> BB4
    -> BB37
BB4[7..9]
    -> BB32
    -> BB5
BB5[10..15]
    -> BB6
    -> BB9
BB6[16..18]
    -> BB7
    -> BB9
BB7[19..19]
    -> BB8
    -> BB9
BB8[20..21]
    -> BB18
BB9[22..24]
    -> BB10
    -> BB34
BB10[25..27]
    -> BB11
    -> BB34
BB11[28..29]
    -> BB12
    -> BB34
BB12[30..30]
    -> BB13
    -> BB34
BB13[31..31]
    -> BB14
    -> BB34
BB14[32..32]
    -> BB15
    -> BB34
BB15[33..34]
    -> BB16
    -> BB34
BB16[35..36]
    -> BB18
    -> BB17
BB17[37..40]
    -> BB18
    -> BB34
BB18[41..43]
    -> BB32
    -> BB19
BB19[44..46]
    -> BB20
    -> BB34
BB20[47..48]
    -> BB21
    -> BB34
BB21[49..51]
    -> BB22
    -> BB34
BB22[52..54]
    -> BB25
    -> BB23
BB23[55..56]
    -> BB24
    -> BB34
BB24[57..57]
    -> BB26
BB25[58..58]
    -> BB26
BB26[59..59]
    -> BB27
    -> BB34
BB27[60..60]
    -> BB28
    -> BB34
BB28[61..61]
    -> BB29
    -> BB34
BB29[62..62]
    -> BB30
    -> BB34
BB30[63..65]
    -> BB31
    -> BB34
BB31[66..66]
    -> BB32
BB32[67..68]
    -> BB33
    -> BB34
BB33[69..69]
    -> BB36
BB34[70..71]
    -> BB35
    -> BB34
BB35[72..72]
    -> BB37
BB36[73..74]
    -> BB37
BB37[-1..-2]
Instructions:
BB0
BB1
0   v2 = getstatic < Application, Lorg/apache/catalina/tribes/io/BufferPool, instance, <Application,Lorg/apache/catalina/tribes/io/BufferPool> >(line 58)
2   conditional branch(ne) v2,v3:#null       (line 58)
BB2
3   v4 = load_metadata: <Primordial,Lorg/apache/catalina/tribes/io/BufferPool>, <Primordial,Ljava/lang/Class>(line 59)
BB3
6   monitorenter v4                          (line 59)
BB4
7   v5 = getstatic < Application, Lorg/apache/catalina/tribes/io/BufferPool, instance, <Application,Lorg/apache/catalina/tribes/io/BufferPool> >(line 60)
9   conditional branch(ne) v5,v3:#null       (line 60)
BB5
15   v8 = invokestatic < Application, Ljava/lang/Class, forName(Ljava/lang/String;)Ljava/lang/Class; > v6:#org.apache.catalina.tribes.io.BufferPool15Impl @23 exception:v7(line 65)
BB6
18   v10 = invokevirtual < Application, Ljava/lang/Class, newInstance()Ljava/lang/Object; > v8 @28 exception:v9(line 66)
BB7
19   v11 = checkcast <Application,Lorg/apache/catalina/tribes/io/BufferPool$BufferPoolAPI>v10(line 66)
BB8
21   goto                                    (line 66)
BB9<Handler>
           v13 = phi  v3:#null,v8,v8
           v12 = getCaughtException 
23   v14 = getstatic < Application, Lorg/apache/catalina/tribes/io/BufferPool, log, <Application,Lorg/apache/juli/logging/Log> >(line 68)
24   v15 = new <Application,Ljava/lang/StringBuilder>@42(line 68)
BB10
27   invokespecial < Application, Ljava/lang/StringBuilder, <init>(Ljava/lang/String;)V > v15,v16:#Unable to initilize BufferPool, not pooling XByteBuffer objects: @48 exception:v17(line 68)
BB11
29   v19 = invokevirtual < Application, Ljava/lang/Throwable, getMessage()Ljava/lang/String; > v12 @52 exception:v18(line 68)
BB12
30   v21 = invokevirtual < Application, Ljava/lang/StringBuilder, append(Ljava/lang/String;)Ljava/lang/StringBuilder; > v15,v19 @55 exception:v20(line 68)
BB13
31   v23 = invokevirtual < Application, Ljava/lang/StringBuilder, toString()Ljava/lang/String; > v21 @58 exception:v22(line 68)
BB14
32   invokeinterface < Application, Lorg/apache/juli/logging/Log, warn(Ljava/lang/Object;)V > v14,v23 @61 exception:v24(line 68)
BB15
33   v25 = getstatic < Application, Lorg/apache/catalina/tribes/io/BufferPool, log, <Application,Lorg/apache/juli/logging/Log> >(line 69)
34   v27 = invokeinterface < Application, Lorg/apache/juli/logging/Log, isDebugEnabled()Z > v25 @69 exception:v26(line 69)
BB16
36   conditional branch(eq) v27,v28:#0       (line 69)
BB17
37   v29 = getstatic < Application, Lorg/apache/catalina/tribes/io/BufferPool, log, <Application,Lorg/apache/juli/logging/Log> >(line 69)
40   invokeinterface < Application, Lorg/apache/juli/logging/Log, debug(Ljava/lang/Object;Ljava/lang/Throwable;)V > v29,v16:#Unable to initilize BufferPool, not pooling XByteBuffer objects:,v12 @83 exception:v30(line 69)
BB18
           v32 = phi  v11,v3:#null,v3:#null
           v33 = phi  v8,v13,v13
43   conditional branch(eq) v32,v3:#null     (line 71)
BB19
46   invokeinterface < Application, Lorg/apache/catalina/tribes/io/BufferPool$BufferPoolAPI, setMaxSize(I)V > v32,v34:#104857600 @95 exception:v35(line 72)
BB20
47   v36 = getstatic < Application, Lorg/apache/catalina/tribes/io/BufferPool, log, <Application,Lorg/apache/juli/logging/Log> >(line 73)
48   v37 = new <Application,Ljava/lang/StringBuilder>@103(line 73)
BB21
51   invokespecial < Application, Ljava/lang/StringBuilder, <init>(Ljava/lang/String;)V > v37,v38:#Created a buffer pool with max size:104857600 bytes of type: @109 exception:v39(line 73)
BB22
54   conditional branch(eq) v33,v3:#null     (line 73)
BB23
56   v42 = invokevirtual < Application, Ljava/lang/Class, getName()Ljava/lang/String; > v33 @117 exception:v41(line 73)
BB24
57   goto                                    (line 73)
BB25
BB26
           v43 = phi  v42,v40:#null
59   v45 = invokevirtual < Application, Ljava/lang/StringBuilder, append(Ljava/lang/String;)Ljava/lang/StringBuilder; > v37,v43 @125 exception:v44(line 73)
BB27
60   v47 = invokevirtual < Application, Ljava/lang/StringBuilder, toString()Ljava/lang/String; > v45 @128 exception:v46(line 73)
BB28
61   invokeinterface < Application, Lorg/apache/juli/logging/Log, info(Ljava/lang/Object;)V > v36,v47 @131 exception:v48(line 73)
BB29
62   v49 = new <Application,Lorg/apache/catalina/tribes/io/BufferPool>@136(line 74)
BB30
65   invokespecial < Application, Lorg/apache/catalina/tribes/io/BufferPool, <init>(Lorg/apache/catalina/tribes/io/BufferPool$BufferPoolAPI;)V > v49,v32 @141 exception:v50(line 74)
BB31
66   putstatic v49 < Application, Lorg/apache/catalina/tribes/io/BufferPool, instance, <Application,Lorg/apache/catalina/tribes/io/BufferPool> >(line 74)
BB32
68   monitorexit v4                          (line 59)
BB33
69   goto                                    (line 59)
BB34<Handler>
           v52 = getCaughtException 
71   monitorexit v4                          (line 59)
BB35
72   throw v52                               (line 59)
BB36
73   v56 = getstatic < Application, Lorg/apache/catalina/tribes/io/BufferPool, instance, <Application,Lorg/apache/catalina/tribes/io/BufferPool> >(line 79)
74   return v56                              (line 79)
BB37

**CGNode:** Node: < Application, Lorg/apache/catalina/tribes/io/BufferPool, <clinit>()V > Context: Everywhere
**IR:** < Application, Lorg/apache/catalina/tribes/io/BufferPool, <clinit>()V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..0]
    -> BB2
    -> BB4
BB2[1..1]
    -> BB3
    -> BB4
BB3[2..5]
    -> BB4
BB4[-1..-2]
Instructions:
BB0
BB1
0   v2 = load_metadata: <Primordial,Lorg/apache/catalina/tribes/io/BufferPool>, <Primordial,Ljava/lang/Class>(line 30)
BB2
1   v4 = invokestatic < Application, Lorg/apache/juli/logging/LogFactory, getLog(Ljava/lang/Class;)Lorg/apache/juli/logging/Log; > v2 @2 exception:v3(line 30)
BB3
2   putstatic v4 < Application, Lorg/apache/catalina/tribes/io/BufferPool, log, <Application,Lorg/apache/juli/logging/Log> >(line 30)
4   putstatic v5:#null < Application, Lorg/apache/catalina/tribes/io/BufferPool, instance, <Application,Lorg/apache/catalina/tribes/io/BufferPool> >(line 36)
5   return                                   (line 29)
BB4

**CGNode:** Node: < Application, Lorg/apache/catalina/tribes/io/ChannelData, <init>(Z)V > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/io/ChannelData, getDataFromPackage(Lorg/apache/catalina/tribes/io/XByteBuffer;)Lorg/apache/catalina/tribes/io/ChannelData; >:NEW <Application,Lorg/apache/catalina/tribes/io/ChannelData>@0 in ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, main([Ljava/lang/String;)V >:NEW <Application,Lorg/apache/catalina/tribes/io/XByteBuffer>@19 in ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,[Ljava/lang/String>@1 in Everywhere} ]} ]} ]
**IR:** < Application, Lorg/apache/catalina/tribes/io/ChannelData, <init>(Z)V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..1]
    -> BB2
    -> BB6
BB2[2..4]
    -> BB3
    -> BB6
BB3[5..7]
    -> BB5
    -> BB4
BB4[8..9]
    -> BB5
    -> BB6
BB5[10..10]
    -> BB6
BB6[-1..-2]
Instructions:
BB0
BB1
1   invokespecial < Application, Ljava/lang/Object, <init>()V > v1 @1 exception:v4(line 78)
BB2
4   putfield v1 = v5:#0 < Application, Lorg/apache/catalina/tribes/io/ChannelData, options, <Primordial,I> >(line 48)
BB3
7   conditional branch(eq) v2,v5:#0          (line 79)
BB4
9   invokevirtual < Application, Lorg/apache/catalina/tribes/io/ChannelData, generateUUID()V > v1 @14 exception:v6(line 79)
BB5
10   return                                  (line 80)
BB6

**CGNode:** Node: < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, toInt([BI)I > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, main([Ljava/lang/String;)V >:NEW <Application,Lorg/apache/catalina/tribes/io/XByteBuffer>@19 in ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,[Ljava/lang/String>@1 in Everywhere} ]} ]
**IR:** < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, toInt([BI)I >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..4]
    -> BB2
    -> BB6
BB2[5..11]
    -> BB3
    -> BB6
BB3[12..21]
    -> BB4
    -> BB6
BB4[22..31]
    -> BB5
    -> BB6
BB5[32..37]
    -> BB6
BB6[-1..-2]
Instructions:
BB0
BB1
3   v5 = binaryop(add) v2 , v4:#3            (line 396)
4   v6 = arrayload v1[v5]                    (line 396)
BB2
6   v8 = binaryop(and) v6 , v7:#255          (line 396)
10   v10 = binaryop(add) v2 , v9:#2          (line 397)
11   v11 = arrayload v1[v10]                 (line 397)
BB3
13   v12 = binaryop(and) v11 , v7:#255       (line 397)
15   v14 = binaryop(SHL) v12 , v13:#8        (line 397)
16   v15 = binaryop(add) v8 , v14            (line 396)
20   v17 = binaryop(add) v2 , v16:#1         (line 398)
21   v18 = arrayload v1[v17]                 (line 398)
BB4
23   v19 = binaryop(and) v18 , v7:#255       (line 398)
25   v21 = binaryop(SHL) v19 , v20:#16       (line 398)
26   v22 = binaryop(add) v15 , v21           (line 396)
30   v24 = binaryop(add) v2 , v23:#0         (line 399)
31   v25 = arrayload v1[v24]                 (line 399)
BB5
33   v26 = binaryop(and) v25 , v7:#255       (line 399)
35   v28 = binaryop(SHL) v26 , v27:#24       (line 399)
36   v29 = binaryop(add) v22 , v28           (line 396)
37   return v29                              (line 396)
BB6

**CGNode:** Node: < Application, Lorg/apache/catalina/tribes/io/ChannelData, setOptions(I)V > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/io/ChannelData, getDataFromPackage(Lorg/apache/catalina/tribes/io/XByteBuffer;)Lorg/apache/catalina/tribes/io/ChannelData; >:NEW <Application,Lorg/apache/catalina/tribes/io/ChannelData>@0 in ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, main([Ljava/lang/String;)V >:NEW <Application,Lorg/apache/catalina/tribes/io/XByteBuffer>@19 in ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,[Ljava/lang/String>@1 in Everywhere} ]} ]} ]
**IR:** < Application, Lorg/apache/catalina/tribes/io/ChannelData, setOptions(I)V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..2]
    -> BB2
    -> BB3
BB2[3..3]
    -> BB3
BB3[-1..-2]
Instructions:
BB0
BB1
2   putfield v1 = v2 < Application, Lorg/apache/catalina/tribes/io/ChannelData, options, <Primordial,I> >(line 152)
BB2
3   return                                   (line 153)
BB3

**CGNode:** Node: < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, toLong([BI)J > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, main([Ljava/lang/String;)V >:NEW <Application,Lorg/apache/catalina/tribes/io/XByteBuffer>@19 in ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,[Ljava/lang/String>@1 in Everywhere} ]} ]
**IR:** < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, toLong([BI)J >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..4]
    -> BB2
    -> BB10
BB2[5..12]
    -> BB3
    -> BB10
BB3[13..23]
    -> BB4
    -> BB10
BB4[24..34]
    -> BB5
    -> BB10
BB5[35..45]
    -> BB6
    -> BB10
BB6[46..56]
    -> BB7
    -> BB10
BB7[57..67]
    -> BB8
    -> BB10
BB8[68..78]
    -> BB9
    -> BB10
BB9[79..85]
    -> BB10
BB10[-1..-2]
Instructions:
BB0
BB1
3   v5 = binaryop(add) v2 , v4:#7            (line 410)
4   v6 = arrayload v1[v5]                    (line 410)
BB2
5   v7 = conversion(J) v6                    (line 410)
7   v9 = binaryop(and) v7 , v8:#255          (line 410)
11   v11 = binaryop(add) v2 , v10:#6         (line 411)
12   v12 = arrayload v1[v11]                 (line 411)
BB3
13   v13 = conversion(J) v12                 (line 411)
15   v14 = binaryop(and) v13 , v8:#255       (line 411)
17   v16 = binaryop(SHL) v14 , v15:#8        (line 411)
18   v17 = binaryop(add) v9 , v16            (line 410)
22   v19 = binaryop(add) v2 , v18:#5         (line 412)
23   v20 = arrayload v1[v19]                 (line 412)
BB4
24   v21 = conversion(J) v20                 (line 412)
26   v22 = binaryop(and) v21 , v8:#255       (line 412)
28   v24 = binaryop(SHL) v22 , v23:#16       (line 412)
29   v25 = binaryop(add) v17 , v24           (line 410)
33   v27 = binaryop(add) v2 , v26:#4         (line 413)
34   v28 = arrayload v1[v27]                 (line 413)
BB5
35   v29 = conversion(J) v28                 (line 413)
37   v30 = binaryop(and) v29 , v8:#255       (line 413)
39   v32 = binaryop(SHL) v30 , v31:#24       (line 413)
40   v33 = binaryop(add) v25 , v32           (line 410)
44   v35 = binaryop(add) v2 , v34:#3         (line 414)
45   v36 = arrayload v1[v35]                 (line 414)
BB6
46   v37 = conversion(J) v36                 (line 414)
48   v38 = binaryop(and) v37 , v8:#255       (line 414)
50   v40 = binaryop(SHL) v38 , v39:#32       (line 414)
51   v41 = binaryop(add) v33 , v40           (line 410)
55   v43 = binaryop(add) v2 , v42:#2         (line 415)
56   v44 = arrayload v1[v43]                 (line 415)
BB7
57   v45 = conversion(J) v44                 (line 415)
59   v46 = binaryop(and) v45 , v8:#255       (line 415)
61   v48 = binaryop(SHL) v46 , v47:#40       (line 415)
62   v49 = binaryop(add) v41 , v48           (line 410)
66   v51 = binaryop(add) v2 , v50:#1         (line 416)
67   v52 = arrayload v1[v51]                 (line 416)
BB8
68   v53 = conversion(J) v52                 (line 416)
70   v54 = binaryop(and) v53 , v8:#255       (line 416)
72   v56 = binaryop(SHL) v54 , v55:#48       (line 416)
73   v57 = binaryop(add) v49 , v56           (line 410)
77   v59 = binaryop(add) v2 , v58:#0         (line 417)
78   v60 = arrayload v1[v59]                 (line 417)
BB9
79   v61 = conversion(J) v60                 (line 417)
81   v62 = binaryop(and) v61 , v8:#255       (line 417)
83   v64 = binaryop(SHL) v62 , v63:#56       (line 417)
84   v65 = binaryop(add) v57 , v64           (line 410)
85   return v65                              (line 410)
BB10

**CGNode:** Node: < Application, Lorg/apache/catalina/tribes/io/ChannelData, setTimestamp(J)V > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/io/ChannelData, getDataFromPackage(Lorg/apache/catalina/tribes/io/XByteBuffer;)Lorg/apache/catalina/tribes/io/ChannelData; >:NEW <Application,Lorg/apache/catalina/tribes/io/ChannelData>@0 in ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, main([Ljava/lang/String;)V >:NEW <Application,Lorg/apache/catalina/tribes/io/XByteBuffer>@19 in ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,[Ljava/lang/String>@1 in Everywhere} ]} ]} ]
**IR:** < Application, Lorg/apache/catalina/tribes/io/ChannelData, setTimestamp(J)V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..2]
    -> BB2
    -> BB3
BB2[3..3]
    -> BB3
BB3[-1..-2]
Instructions:
BB0
BB1
2   putfield v1 = v2 < Application, Lorg/apache/catalina/tribes/io/ChannelData, timestamp, <Primordial,J> >(line 121)
BB2
3   return                                   (line 122)
BB3

**CGNode:** Node: < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, getMember([BII)Lorg/apache/catalina/tribes/membership/MemberImpl; > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, main([Ljava/lang/String;)V >:NEW <Application,Lorg/apache/catalina/tribes/io/XByteBuffer>@19 in ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,[Ljava/lang/String>@1 in Everywhere} ]} ]
**IR:** < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, getMember([BII)Lorg/apache/catalina/tribes/membership/MemberImpl; >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..3]
    -> BB2
    -> BB5
BB2[4..5]
    -> BB3
    -> BB5
BB3[6..6]
    -> BB4
    -> BB5
BB4[7..7]
    -> BB5
BB5[-1..-2]
Instructions:
BB0
BB1
3   v5 = new <Application,Lorg/apache/catalina/tribes/membership/MemberImpl>@3(line 422)
BB2
5   invokespecial < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, <init>()V > v5 @7 exception:v6(line 422)
BB3
6   v8 = invokestatic < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, getMember([BIILorg/apache/catalina/tribes/membership/MemberImpl;)Lorg/apache/catalina/tribes/membership/MemberImpl; > v1,v2,v3,v5 @10 exception:v7(line 422)
BB4
7   return v8                                (line 422)
BB5

**CGNode:** Node: < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, <clinit>()V > Context: Everywhere
**IR:** < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, <clinit>()V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..2]
    -> BB2
    -> BB24
BB2[3..3]
    -> BB3
    -> BB24
BB3[4..6]
    -> BB4
    -> BB24
BB4[7..10]
    -> BB5
    -> BB24
BB5[11..14]
    -> BB6
    -> BB24
BB6[15..18]
    -> BB7
    -> BB24
BB7[19..22]
    -> BB8
    -> BB24
BB8[23..26]
    -> BB9
    -> BB24
BB9[27..30]
    -> BB10
    -> BB24
BB10[31..34]
    -> BB11
    -> BB24
BB11[35..38]
    -> BB12
    -> BB24
BB12[39..42]
    -> BB13
    -> BB24
BB13[43..45]
    -> BB14
    -> BB24
BB14[46..49]
    -> BB15
    -> BB24
BB15[50..53]
    -> BB16
    -> BB24
BB16[54..57]
    -> BB17
    -> BB24
BB17[58..61]
    -> BB18
    -> BB24
BB18[62..65]
    -> BB19
    -> BB24
BB19[66..69]
    -> BB20
    -> BB24
BB20[70..73]
    -> BB21
    -> BB24
BB21[74..77]
    -> BB22
    -> BB24
BB22[78..81]
    -> BB23
    -> BB24
BB23[82..83]
    -> BB24
BB24[-1..-2]
Instructions:
BB0
BB1
2   v5 = invokestatic < Application, Ljava/lang/System, getProperty(Ljava/lang/String;Ljava/lang/String;)Ljava/lang/String; > v2:#org.apache.catalina.tribes.dns_lookups,v3:#false @4 exception:v4(line 43)
BB2
3   v7 = invokestatic < Application, Ljava/lang/Boolean, parseBoolean(Ljava/lang/String;)Z > v5 @7 exception:v6(line 43)
BB3
4   putstatic v7 < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, DO_DNS_LOOKUPS, <Primordial,Z> >(line 43)
6   v9 = new <Primordial,[B>@15v8:#10        (line 51)
BB4
10   arraystore v9[v10:#0] = v11:#84         (line 51)
BB5
14   arraystore v9[v12:#1] = v13:#82         (line 51)
BB6
18   arraystore v9[v14:#2] = v15:#73         (line 51)
BB7
22   arraystore v9[v16:#3] = v17:#66         (line 51)
BB8
26   arraystore v9[v18:#4] = v19:#69         (line 51)
BB9
30   arraystore v9[v20:#5] = v21:#83         (line 51)
BB10
34   arraystore v9[v22:#6] = v23:#45         (line 51)
BB11
38   arraystore v9[v24:#7] = v17:#66         (line 51)
BB12
42   arraystore v9[v25:#8] = v12:#1          (line 51)
BB13
43   putstatic v9 < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, TRIBES_MBR_BEGIN, <Primordial,[B> >(line 51)
45   v26 = new <Primordial,[B>@69v8:#10      (line 52)
BB14
49   arraystore v26[v10:#0] = v11:#84        (line 52)
BB15
53   arraystore v26[v12:#1] = v13:#82        (line 52)
BB16
57   arraystore v26[v14:#2] = v15:#73        (line 52)
BB17
61   arraystore v26[v16:#3] = v17:#66        (line 52)
BB18
65   arraystore v26[v18:#4] = v19:#69        (line 52)
BB19
69   arraystore v26[v20:#5] = v21:#83        (line 52)
BB20
73   arraystore v26[v22:#6] = v23:#45        (line 52)
BB21
77   arraystore v26[v24:#7] = v19:#69        (line 52)
BB22
81   arraystore v26[v25:#8] = v12:#1         (line 52)
BB23
82   putstatic v26 < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, TRIBES_MBR_END, <Primordial,[B> >(line 52)
83   return                                  (line 37)
BB24

**CGNode:** Node: < Application, Lorg/apache/catalina/tribes/io/ChannelData, setAddress(Lorg/apache/catalina/tribes/Member;)V > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/io/ChannelData, getDataFromPackage(Lorg/apache/catalina/tribes/io/XByteBuffer;)Lorg/apache/catalina/tribes/io/ChannelData; >:NEW <Application,Lorg/apache/catalina/tribes/io/ChannelData>@0 in ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, main([Ljava/lang/String;)V >:NEW <Application,Lorg/apache/catalina/tribes/io/XByteBuffer>@19 in ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,[Ljava/lang/String>@1 in Everywhere} ]} ]} ]
**IR:** < Application, Lorg/apache/catalina/tribes/io/ChannelData, setAddress(Lorg/apache/catalina/tribes/Member;)V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..2]
    -> BB2
    -> BB3
BB2[3..3]
    -> BB3
BB3[-1..-2]
Instructions:
BB0
BB1
2   putfield v1 = v2 < Application, Lorg/apache/catalina/tribes/io/ChannelData, address, <Application,Lorg/apache/catalina/tribes/Member> >(line 170)
BB2
3   return                                   (line 171)
BB3

**CGNode:** Node: < Application, Lorg/apache/tomcat/util/net/SocketProperties, <init>()V > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, <init>()V >:NEW <Application,Lorg/apache/tomcat/util/net/SocketProperties>@25 in ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, main([Ljava/lang/String;)V >:NEW <Application,Lorg/apache/tomcat/util/net/AprEndpoint>@0 in ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,[Ljava/lang/String>@6 in Everywhere} ]} ]} ]
**IR:** < Application, Lorg/apache/tomcat/util/net/SocketProperties, <init>()V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..1]
    -> BB2
    -> BB28
BB2[2..4]
    -> BB3
    -> BB28
BB3[5..7]
    -> BB4
    -> BB28
BB4[8..10]
    -> BB5
    -> BB28
BB5[11..13]
    -> BB6
    -> BB28
BB6[14..16]
    -> BB7
    -> BB28
BB7[17..19]
    -> BB8
    -> BB28
BB8[20..22]
    -> BB9
    -> BB28
BB9[23..25]
    -> BB10
    -> BB28
BB10[26..28]
    -> BB11
    -> BB28
BB11[29..31]
    -> BB12
    -> BB28
BB12[32..34]
    -> BB13
    -> BB28
BB13[35..37]
    -> BB14
    -> BB28
BB14[38..40]
    -> BB15
    -> BB28
BB15[41..43]
    -> BB16
    -> BB28
BB16[44..46]
    -> BB17
    -> BB28
BB17[47..49]
    -> BB18
    -> BB28
BB18[50..51]
    -> BB19
    -> BB28
BB19[52..54]
    -> BB20
    -> BB28
BB20[55..55]
    -> BB21
    -> BB28
BB21[56..58]
    -> BB22
    -> BB28
BB22[59..61]
    -> BB23
    -> BB28
BB23[62..64]
    -> BB24
    -> BB28
BB24[65..67]
    -> BB25
    -> BB28
BB25[68..70]
    -> BB26
    -> BB28
BB26[71..73]
    -> BB27
    -> BB28
BB27[74..74]
    -> BB28
BB28[-1..-2]
Instructions:
BB0
BB1
1   invokespecial < Application, Ljava/lang/Object, <init>()V > v1 @1 exception:v3(line 30)
BB2
4   putfield v1 = v4:#500 < Application, Lorg/apache/tomcat/util/net/SocketProperties, keyCache, <Primordial,I> >(line 38)
BB3
7   putfield v1 = v4:#500 < Application, Lorg/apache/tomcat/util/net/SocketProperties, processorCache, <Primordial,I> >(line 47)
BB4
10   putfield v1 = v4:#500 < Application, Lorg/apache/tomcat/util/net/SocketProperties, eventCache, <Primordial,I> >(line 57)
BB5
13   putfield v1 = v5:#0 < Application, Lorg/apache/tomcat/util/net/SocketProperties, directBuffer, <Primordial,Z> >(line 63)
BB6
16   putfield v1 = v6:#null < Application, Lorg/apache/tomcat/util/net/SocketProperties, rxBufSize, <Application,Ljava/lang/Integer> >(line 69)
BB7
19   putfield v1 = v6:#null < Application, Lorg/apache/tomcat/util/net/SocketProperties, txBufSize, <Application,Ljava/lang/Integer> >(line 75)
BB8
22   putfield v1 = v7:#8192 < Application, Lorg/apache/tomcat/util/net/SocketProperties, appReadBufSize, <Primordial,I> >(line 81)
BB9
25   putfield v1 = v7:#8192 < Application, Lorg/apache/tomcat/util/net/SocketProperties, appWriteBufSize, <Primordial,I> >(line 87)
BB10
28   putfield v1 = v4:#500 < Application, Lorg/apache/tomcat/util/net/SocketProperties, bufferPool, <Primordial,I> >(line 95)
BB11
31   putfield v1 = v8:#104857600 < Application, Lorg/apache/tomcat/util/net/SocketProperties, bufferPoolSize, <Primordial,I> >(line 102)
BB12
33   v9 = getstatic < Application, Ljava/lang/Boolean, TRUE, <Application,Ljava/lang/Boolean> >(line 107)
34   putfield v1 = v9 < Application, Lorg/apache/tomcat/util/net/SocketProperties, tcpNoDelay, <Application,Ljava/lang/Boolean> >(line 107)
BB13
37   putfield v1 = v6:#null < Application, Lorg/apache/tomcat/util/net/SocketProperties, soKeepAlive, <Application,Ljava/lang/Boolean> >(line 112)
BB14
40   putfield v1 = v6:#null < Application, Lorg/apache/tomcat/util/net/SocketProperties, ooBInline, <Application,Ljava/lang/Boolean> >(line 117)
BB15
43   putfield v1 = v6:#null < Application, Lorg/apache/tomcat/util/net/SocketProperties, soReuseAddress, <Application,Ljava/lang/Boolean> >(line 122)
BB16
46   putfield v1 = v6:#null < Application, Lorg/apache/tomcat/util/net/SocketProperties, soLingerOn, <Application,Ljava/lang/Boolean> >(line 128)
BB17
49   putfield v1 = v6:#null < Application, Lorg/apache/tomcat/util/net/SocketProperties, soLingerTime, <Application,Ljava/lang/Integer> >(line 134)
BB18
51   v10 = new <Application,Ljava/lang/Integer>@100(line 139)
BB19
54   invokespecial < Application, Ljava/lang/Integer, <init>(I)V > v10,v11:#20000 @107 exception:v12(line 139)
BB20
55   putfield v1 = v10 < Application, Lorg/apache/tomcat/util/net/SocketProperties, soTimeout, <Application,Ljava/lang/Integer> >(line 139)
BB21
58   putfield v1 = v6:#null < Application, Lorg/apache/tomcat/util/net/SocketProperties, soTrafficClass, <Application,Ljava/lang/Integer> >(line 149)
BB22
61   putfield v1 = v6:#null < Application, Lorg/apache/tomcat/util/net/SocketProperties, performanceConnectionTime, <Application,Ljava/lang/Integer> >(line 157)
BB23
64   putfield v1 = v6:#null < Application, Lorg/apache/tomcat/util/net/SocketProperties, performanceLatency, <Application,Ljava/lang/Integer> >(line 165)
BB24
67   putfield v1 = v6:#null < Application, Lorg/apache/tomcat/util/net/SocketProperties, performanceBandwidth, <Application,Ljava/lang/Integer> >(line 173)
BB25
70   putfield v1 = v13:#1000 < Application, Lorg/apache/tomcat/util/net/SocketProperties, timeoutInterval, <Primordial,J> >(line 179)
BB26
73   putfield v1 = v14:#250 < Application, Lorg/apache/tomcat/util/net/SocketProperties, unlockTimeout, <Primordial,I> >(line 184)
BB27
74   return                                  (line 30)
BB28

**CGNode:** Node: < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint$BindState, <clinit>()V > Context: Everywhere
**IR:** < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint$BindState, <clinit>()V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..0]
    -> BB2
    -> BB12
BB2[1..4]
    -> BB3
    -> BB12
BB3[5..6]
    -> BB4
    -> BB12
BB4[7..10]
    -> BB5
    -> BB12
BB5[11..12]
    -> BB6
    -> BB12
BB6[13..16]
    -> BB7
    -> BB12
BB7[17..19]
    -> BB8
    -> BB12
BB8[20..23]
    -> BB9
    -> BB12
BB9[24..27]
    -> BB10
    -> BB12
BB10[28..31]
    -> BB11
    -> BB12
BB11[32..33]
    -> BB12
BB12[-1..-2]
Instructions:
BB0
BB1
0   v2 = new <Application,Lorg/apache/tomcat/util/net/AbstractEndpoint$BindState>@0(line 77)
BB2
4   invokespecial < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint$BindState, <init>(Ljava/lang/String;I)V > v2,v3:#UNBOUND,v4:#0 @7 exception:v5(line 77)
BB3
5   putstatic v2 < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint$BindState, UNBOUND, <Application,Lorg/apache/tomcat/util/net/AbstractEndpoint$BindState> >(line 77)
6   v6 = new <Application,Lorg/apache/tomcat/util/net/AbstractEndpoint$BindState>@13(line 77)
BB4
10   invokespecial < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint$BindState, <init>(Ljava/lang/String;I)V > v6,v7:#BOUND_ON_INIT,v8:#1 @20 exception:v9(line 77)
BB5
11   putstatic v6 < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint$BindState, BOUND_ON_INIT, <Application,Lorg/apache/tomcat/util/net/AbstractEndpoint$BindState> >(line 77)
12   v10 = new <Application,Lorg/apache/tomcat/util/net/AbstractEndpoint$BindState>@26(line 77)
BB6
16   invokespecial < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint$BindState, <init>(Ljava/lang/String;I)V > v10,v11:#BOUND_ON_START,v12:#2 @33 exception:v13(line 77)
BB7
17   putstatic v10 < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint$BindState, BOUND_ON_START, <Application,Lorg/apache/tomcat/util/net/AbstractEndpoint$BindState> >(line 77)
19   v15 = new <Application,[Lorg/apache/tomcat/util/net/AbstractEndpoint$BindState>@40v14:#3 (line 76)
BB8
22   v16 = getstatic < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint$BindState, UNBOUND, <Application,Lorg/apache/tomcat/util/net/AbstractEndpoint$BindState> >(line 76)
23   arraystore v15[v4:#0] = v16             (line 76)
BB9
26   v17 = getstatic < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint$BindState, BOUND_ON_INIT, <Application,Lorg/apache/tomcat/util/net/AbstractEndpoint$BindState> >(line 76)
27   arraystore v15[v8:#1] = v17             (line 76)
BB10
30   v18 = getstatic < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint$BindState, BOUND_ON_START, <Application,Lorg/apache/tomcat/util/net/AbstractEndpoint$BindState> >(line 76)
31   arraystore v15[v12:#2] = v18            (line 76)
BB11
32   putstatic v15 < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint$BindState, ENUM$VALUES, <Application,[Lorg/apache/tomcat/util/net/AbstractEndpoint$BindState> >(line 76)
33   return                                  (line 76)
BB12

**CGNode:** Node: < Application, Lorg/apache/tomcat/util/net/AprEndpoint$Acceptor, <init>(Lorg/apache/tomcat/util/net/AprEndpoint;)V > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/tomcat/util/net/AprEndpoint, createAcceptor()Lorg/apache/tomcat/util/net/AbstractEndpoint$Acceptor; >:NEW <Application,Lorg/apache/tomcat/util/net/AprEndpoint$Acceptor>@0 in ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, main([Ljava/lang/String;)V >:NEW <Application,Lorg/apache/tomcat/util/net/AprEndpoint>@0 in ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,[Ljava/lang/String>@6 in Everywhere} ]} ]} ]
**IR:** < Application, Lorg/apache/tomcat/util/net/AprEndpoint$Acceptor, <init>(Lorg/apache/tomcat/util/net/AprEndpoint;)V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..2]
    -> BB2
    -> BB7
BB2[3..4]
    -> BB3
    -> BB7
BB3[5..6]
    -> BB4
    -> BB7
BB4[7..7]
    -> BB5
    -> BB7
BB5[8..8]
    -> BB6
    -> BB7
BB6[9..9]
    -> BB7
BB7[-1..-2]
Instructions:
BB0
BB1
2   putfield v1 = v2 < Application, Lorg/apache/tomcat/util/net/AprEndpoint$Acceptor, this$0, <Application,Lorg/apache/tomcat/util/net/AprEndpoint> >(line 961)
BB2
4   invokespecial < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint$Acceptor, <init>()V > v1 @6 exception:v4(line 961)
BB3
6   v5 = load_metadata: <Primordial,Lorg/apache/tomcat/util/net/AprEndpoint$Acceptor>, <Primordial,Ljava/lang/Class>(line 963)
BB4
7   v7 = invokestatic < Application, Lorg/apache/juli/logging/LogFactory, getLog(Ljava/lang/Class;)Lorg/apache/juli/logging/Log; > v5 @12 exception:v6(line 963)
BB5
8   putfield v1 = v7 < Application, Lorg/apache/tomcat/util/net/AprEndpoint$Acceptor, log, <Application,Lorg/apache/juli/logging/Log> >(line 963)
BB6
9   return                                   (line 963)
BB7

**CGNode:** Node: < Application, Lorg/apache/tomcat/util/res/StringManager, <init>(Ljava/lang/String;Ljava/util/Locale;)V > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/tomcat/util/res/StringManager, getManager(Ljava/lang/String;Ljava/util/Locale;)Lorg/apache/tomcat/util/res/StringManager; >:NEW <Application,Lorg/apache/tomcat/util/res/StringManager>@51 in ReceiverStringContext: [ [<Primordial,Ljava/lang/String>] ]} ]
**IR:** < Application, Lorg/apache/tomcat/util/res/StringManager, <init>(Ljava/lang/String;Ljava/util/Locale;)V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..1]
    -> BB2
    -> BB24
BB2[2..2]
    -> BB3
    -> BB24
BB3[3..5]
    -> BB4
    -> BB24
BB4[6..6]
    -> BB5
    -> BB24
BB5[7..8]
    -> BB6
    -> BB24
BB6[9..9]
    -> BB7
    -> BB24
BB7[10..15]
    -> BB8
    -> BB9
    -> BB24
BB8[16..17]
    -> BB15
BB9[18..19]
    -> BB10
    -> BB24
BB10[20..20]
    -> BB11
    -> BB24
BB11[21..24]
    -> BB15
    -> BB12
BB12[25..28]
    -> BB13
    -> BB14
    -> BB24
BB13[29..30]
    -> BB15
BB14[31..31]
    -> BB15
BB15[32..34]
    -> BB16
    -> BB24
BB16[35..36]
    -> BB17
    -> BB24
BB17[37..38]
    -> BB22
    -> BB18
BB18[39..41]
    -> BB19
    -> BB24
BB19[42..42]
    -> BB20
    -> BB24
BB20[43..43]
    -> BB21
    -> BB24
BB21[44..44]
    -> BB23
BB22[45..47]
    -> BB23
    -> BB24
BB23[48..48]
    -> BB24
BB24[-1..-2]
Instructions:
BB0
BB1
1   invokespecial < Application, Ljava/lang/Object, <init>()V > v1 @1 exception:v5(line 70)
BB2
2   v6 = new <Application,Ljava/lang/StringBuilder>@4(line 71)
BB3
5   v8 = invokestatic < Application, Ljava/lang/String, valueOf(Ljava/lang/Object;)Ljava/lang/String; > v2 @9 exception:v7(line 71)
BB4
6   invokespecial < Application, Ljava/lang/StringBuilder, <init>(Ljava/lang/String;)V > v6,v8 @12 exception:v9(line 71)
BB5
8   v12 = invokevirtual < Application, Ljava/lang/StringBuilder, append(Ljava/lang/String;)Ljava/lang/StringBuilder; > v6,v10:#.LocalStrings @17 exception:v11(line 71)
BB6
9   v14 = invokevirtual < Application, Ljava/lang/StringBuilder, toString()Ljava/lang/String; > v12 @20 exception:v13(line 71)
BB7
15   v17 = invokestatic < Application, Ljava/util/ResourceBundle, getBundle(Ljava/lang/String;Ljava/util/Locale;)Ljava/util/ResourceBundle; > v14,v3 @29 exception:v16(line 74)
BB8
17   goto                                    (line 74)
BB9<Handler>
           v18 = getCaughtException 
19   v20 = invokestatic < Application, Ljava/lang/Thread, currentThread()Ljava/lang/Thread; > @39 exception:v19(line 79)
BB10
20   v22 = invokevirtual < Application, Ljava/lang/Thread, getContextClassLoader()Ljava/lang/ClassLoader; > v20 @42 exception:v21(line 79)
BB11
24   conditional branch(eq) v22,v15:#null    (line 80)
BB12
28   v24 = invokestatic < Application, Ljava/util/ResourceBundle, getBundle(Ljava/lang/String;Ljava/util/Locale;Ljava/lang/ClassLoader;)Ljava/util/ResourceBundle; > v14,v3,v22 @56 exception:v23(line 82)
BB13
30   goto                                    (line 82)
BB14<Handler>
           v25 = getCaughtException 
BB15
           v27 = phi  v17,v15:#null,v24,v15:#null
34   putfield v1 = v27 < Application, Lorg/apache/tomcat/util/res/StringManager, bundle, <Application,Ljava/util/ResourceBundle> >(line 88)
BB16
36   v28 = getfield < Application, Lorg/apache/tomcat/util/res/StringManager, bundle, <Application,Ljava/util/ResourceBundle> > v1(line 90)
BB17
38   conditional branch(eq) v28,v15:#null    (line 90)
BB18
41   v29 = getfield < Application, Lorg/apache/tomcat/util/res/StringManager, bundle, <Application,Ljava/util/ResourceBundle> > v1(line 91)
BB19
42   v31 = invokevirtual < Application, Ljava/util/ResourceBundle, getLocale()Ljava/util/Locale; > v29 @84 exception:v30(line 91)
BB20
43   putfield v1 = v31 < Application, Lorg/apache/tomcat/util/res/StringManager, locale, <Application,Ljava/util/Locale> >(line 91)
BB21
44   goto                                    (line 91)
BB22
47   putfield v1 = v15:#null < Application, Lorg/apache/tomcat/util/res/StringManager, locale, <Application,Ljava/util/Locale> >(line 93)
BB23
48   return                                  (line 95)
BB24

**CGNode:** Node: < Application, Lorg/apache/catalina/tribes/transport/bio/util/SingleRemoveSynchronizedAddLock, lockRemove()Z > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/transport/bio/util/FastQueue, <init>()V >:NEW <Application,Lorg/apache/catalina/tribes/transport/bio/util/SingleRemoveSynchronizedAddLock>@49 in ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/group/interceptors/MessageDispatchInterceptor, <init>()V >:NEW <Application,Lorg/apache/catalina/tribes/transport/bio/util/FastQueue>@12 in ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,Lorg/apache/catalina/tribes/group/interceptors/MessageDispatchInterceptor>@11 in Everywhere} ]} ]} ]
**IR:** < Application, Lorg/apache/catalina/tribes/transport/bio/util/SingleRemoveSynchronizedAddLock, lockRemove()Z >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..2]
    -> BB2
    -> BB28
BB2[3..5]
    -> BB3
    -> BB28
BB3[6..7]
    -> BB4
    -> BB28
BB4[8..9]
    -> BB7
    -> BB5
BB5[10..11]
    -> BB6
    -> BB28
BB6[12..13]
    -> BB23
    -> BB7
BB7[14..15]
    -> BB8
    -> BB28
BB8[16..17]
    -> BB23
    -> BB9
BB9[18..19]
    -> BB10
    -> BB28
BB10[20..20]
    -> BB11
    -> BB28
BB11[21..23]
    -> BB12
    -> BB28
BB12[24..24]
    -> BB13
    -> BB14
    -> BB28
BB13[25..25]
    -> BB16
BB14[26..27]
    -> BB15
    -> BB28
BB15[28..28]
    -> BB16
    -> BB28
BB16[29..30]
    -> BB17
    -> BB28
BB17[31..32]
    -> BB20
    -> BB18
BB18[33..34]
    -> BB19
    -> BB28
BB19[35..36]
    -> BB22
    -> BB20
BB20[37..38]
    -> BB21
    -> BB28
BB21[39..40]
    -> BB11
    -> BB22
BB22[41..43]
    -> BB23
    -> BB28
BB23[44..45]
    -> BB24
    -> BB28
BB24[46..47]
    -> BB26
    -> BB25
BB25[48..50]
    -> BB26
    -> BB28
BB26[51..52]
    -> BB27
    -> BB28
BB27[53..53]
    -> BB28
BB28[-1..-2]
Instructions:
BB0
BB1
2   putfield v1 = v3:#0 < Application, Lorg/apache/catalina/tribes/transport/bio/util/SingleRemoveSynchronizedAddLock, removeLocked, <Primordial,Z> >(line 201)
BB2
5   putfield v1 = v4:#1 < Application, Lorg/apache/catalina/tribes/transport/bio/util/SingleRemoveSynchronizedAddLock, removeEnabled, <Primordial,Z> >(line 202)
BB3
7   v5 = getfield < Application, Lorg/apache/catalina/tribes/transport/bio/util/SingleRemoveSynchronizedAddLock, addLocked, <Primordial,Z> > v1(line 203)
BB4
9   conditional branch(ne) v5,v3:#0          (line 203)
BB5
11   v6 = getfield < Application, Lorg/apache/catalina/tribes/transport/bio/util/SingleRemoveSynchronizedAddLock, dataAvailable, <Primordial,Z> > v1(line 203)
BB6
13   conditional branch(ne) v6,v3:#0         (line 203)
BB7
15   v7 = getfield < Application, Lorg/apache/catalina/tribes/transport/bio/util/SingleRemoveSynchronizedAddLock, removeEnabled, <Primordial,Z> > v1(line 203)
BB8
17   conditional branch(eq) v7,v3:#0         (line 203)
BB9
19   v9 = invokestatic < Application, Ljava/lang/Thread, currentThread()Ljava/lang/Thread; > @32 exception:v8(line 204)
BB10
20   putfield v1 = v9 < Application, Lorg/apache/catalina/tribes/transport/bio/util/SingleRemoveSynchronizedAddLock, remover, <Application,Ljava/lang/Thread> >(line 204)
BB11
23   v10 = getfield < Application, Lorg/apache/catalina/tribes/transport/bio/util/SingleRemoveSynchronizedAddLock, removeWaitTimeout, <Primordial,J> > v1(line 207)
BB12
24   invokevirtual < Application, Ljava/lang/Object, wait(J)V > v1,v10 @43 exception:v11(line 207)
BB13
25   goto                                    (line 207)
BB14<Handler>
           v12 = getCaughtException 
27   v14 = invokestatic < Application, Ljava/lang/Thread, currentThread()Ljava/lang/Thread; > @50 exception:v13(line 209)
BB15
28   invokevirtual < Application, Ljava/lang/Thread, interrupt()V > v14 @53 exception:v15(line 209)
BB16
30   v17 = getfield < Application, Lorg/apache/catalina/tribes/transport/bio/util/SingleRemoveSynchronizedAddLock, addLocked, <Primordial,Z> > v1(line 211)
BB17
32   conditional branch(ne) v17,v3:#0        (line 211)
BB18
34   v18 = getfield < Application, Lorg/apache/catalina/tribes/transport/bio/util/SingleRemoveSynchronizedAddLock, dataAvailable, <Primordial,Z> > v1(line 211)
BB19
36   conditional branch(ne) v18,v3:#0        (line 211)
BB20
38   v19 = getfield < Application, Lorg/apache/catalina/tribes/transport/bio/util/SingleRemoveSynchronizedAddLock, removeEnabled, <Primordial,Z> > v1(line 211)
BB21
40   conditional branch(ne) v19,v3:#0        (line 205)
BB22
43   putfield v1 = v21:#null < Application, Lorg/apache/catalina/tribes/transport/bio/util/SingleRemoveSynchronizedAddLock, remover, <Application,Ljava/lang/Thread> >(line 212)
BB23
45   v23 = getfield < Application, Lorg/apache/catalina/tribes/transport/bio/util/SingleRemoveSynchronizedAddLock, removeEnabled, <Primordial,Z> > v1(line 214)
BB24
47   conditional branch(eq) v23,v3:#0        (line 214)
BB25
50   putfield v1 = v4:#1 < Application, Lorg/apache/catalina/tribes/transport/bio/util/SingleRemoveSynchronizedAddLock, removeLocked, <Primordial,Z> >(line 215)
BB26
52   v24 = getfield < Application, Lorg/apache/catalina/tribes/transport/bio/util/SingleRemoveSynchronizedAddLock, removeLocked, <Primordial,Z> > v1(line 217)
BB27
53   return v24                              (line 217)
BB28

**CGNode:** Node: < Application, Lorg/apache/catalina/tribes/transport/bio/util/SingleRemoveSynchronizedAddLock, unlockRemove()V > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/transport/bio/util/FastQueue, <init>()V >:NEW <Application,Lorg/apache/catalina/tribes/transport/bio/util/SingleRemoveSynchronizedAddLock>@49 in ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/group/interceptors/MessageDispatchInterceptor, <init>()V >:NEW <Application,Lorg/apache/catalina/tribes/transport/bio/util/FastQueue>@12 in ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,Lorg/apache/catalina/tribes/group/interceptors/MessageDispatchInterceptor>@11 in Everywhere} ]} ]} ]
**IR:** < Application, Lorg/apache/catalina/tribes/transport/bio/util/SingleRemoveSynchronizedAddLock, unlockRemove()V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..2]
    -> BB2
    -> BB5
BB2[3..5]
    -> BB3
    -> BB5
BB3[6..7]
    -> BB4
    -> BB5
BB4[8..8]
    -> BB5
BB5[-1..-2]
Instructions:
BB0
BB1
2   putfield v1 = v3:#0 < Application, Lorg/apache/catalina/tribes/transport/bio/util/SingleRemoveSynchronizedAddLock, removeLocked, <Primordial,Z> >(line 240)
BB2
5   putfield v1 = v3:#0 < Application, Lorg/apache/catalina/tribes/transport/bio/util/SingleRemoveSynchronizedAddLock, dataAvailable, <Primordial,Z> >(line 241)
BB3
7   invokevirtual < Application, Ljava/lang/Object, notifyAll()V > v1 @11 exception:v4(line 242)
BB4
8   return                                   (line 243)
BB5

**CGNode:** Node: < Application, Lorg/apache/catalina/tribes/group/ChannelInterceptorBase, getNext()Lorg/apache/catalina/tribes/ChannelInterceptor; > Context: ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,Lorg/apache/catalina/tribes/group/interceptors/MessageDispatchInterceptor>@11 in Everywhere} ]
**IR:** < Application, Lorg/apache/catalina/tribes/group/ChannelInterceptorBase, getNext()Lorg/apache/catalina/tribes/ChannelInterceptor; >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..1]
    -> BB2
    -> BB3
BB2[2..2]
    -> BB3
BB3[-1..-2]
Instructions:
BB0
BB1
1   v3 = getfield < Application, Lorg/apache/catalina/tribes/group/ChannelInterceptorBase, next, <Application,Lorg/apache/catalina/tribes/ChannelInterceptor> > v1(line 53)
BB2
2   return v3                                (line 53)
BB3

**CGNode:** Node: < Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, printStats(JDILjava/text/DecimalFormat;Ljava/math/BigDecimal;)V > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, main([Ljava/lang/String;)V >:NEW <Application,Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive$1>@68 in ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,[Ljava/lang/String>@1 in Everywhere} ]} ]
**IR:** < Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, printStats(JDILjava/text/DecimalFormat;Ljava/math/BigDecimal;)V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..0]
    -> BB2
    -> BB16
BB2[1..10]
    -> BB3
    -> BB16
BB3[11..13]
    -> BB4
    -> BB16
BB4[14..18]
    -> BB5
    -> BB16
BB5[19..19]
    -> BB6
    -> BB16
BB6[20..21]
    -> BB7
    -> BB16
BB7[22..23]
    -> BB8
    -> BB16
BB8[24..25]
    -> BB9
    -> BB16
BB9[26..27]
    -> BB10
    -> BB16
BB10[28..29]
    -> BB11
    -> BB16
BB11[30..31]
    -> BB12
    -> BB16
BB12[32..33]
    -> BB13
    -> BB16
BB13[34..34]
    -> BB14
    -> BB16
BB14[35..35]
    -> BB15
    -> BB16
BB15[36..36]
    -> BB16
BB16[-1..-2]
Instructions:
BB0
BB1
0   v8 = invokestatic < Application, Ljava/lang/System, currentTimeMillis()J > @0 exception:v7(line 88)
BB2
4   v9 = binaryop(sub) v8 , v1               (line 89)
5   v10 = conversion(D) v9                   (line 89)
7   v12 = binaryop(div) v10 , v11:#1000.0    (line 89)
9   v13 = getstatic < Application, Ljava/lang/System, out, <Application,Ljava/io/PrintStream> >(line 90)
10   v14 = new <Application,Ljava/lang/StringBuilder>@19(line 90)
BB3
13   invokespecial < Application, Ljava/lang/StringBuilder, <init>(Ljava/lang/String;)V > v14,v15:#Throughput  @25 exception:v16(line 90)
BB4
17   v17 = binaryop(div) v2 , v12            (line 90)
18   v19 = invokevirtual < Application, Ljava/text/DecimalFormat, format(D)Ljava/lang/String; > v4,v17 @34 exception:v18(line 90)
BB5
19   v21 = invokevirtual < Application, Ljava/lang/StringBuilder, append(Ljava/lang/String;)Ljava/lang/StringBuilder; > v14,v19 @37 exception:v20(line 90)
BB6
21   v24 = invokevirtual < Application, Ljava/lang/StringBuilder, append(Ljava/lang/String;)Ljava/lang/StringBuilder; > v21,v22:# MB/seconds messages  @42 exception:v23(line 90)
BB7
23   v26 = invokevirtual < Application, Ljava/lang/StringBuilder, append(I)Ljava/lang/StringBuilder; > v24,v3 @47 exception:v25(line 90)
BB8
25   v29 = invokevirtual < Application, Ljava/lang/StringBuilder, append(Ljava/lang/String;)Ljava/lang/StringBuilder; > v26,v27:#, total  @52 exception:v28(line 90)
BB9
27   v31 = invokevirtual < Application, Ljava/lang/StringBuilder, append(D)Ljava/lang/StringBuilder; > v29,v2 @56 exception:v30(line 90)
BB10
29   v34 = invokevirtual < Application, Ljava/lang/StringBuilder, append(Ljava/lang/String;)Ljava/lang/StringBuilder; > v31,v32:# MB, total  @61 exception:v33(line 90)
BB11
31   v36 = invokevirtual < Application, Ljava/lang/StringBuilder, append(Ljava/lang/Object;)Ljava/lang/StringBuilder; > v34,v5 @66 exception:v35(line 90)
BB12
33   v39 = invokevirtual < Application, Ljava/lang/StringBuilder, append(Ljava/lang/String;)Ljava/lang/StringBuilder; > v36,v37:# bytes. @71 exception:v38(line 90)
BB13
34   v41 = invokevirtual < Application, Ljava/lang/StringBuilder, toString()Ljava/lang/String; > v39 @74 exception:v40(line 90)
BB14
35   invokevirtual < Application, Ljava/io/PrintStream, println(Ljava/lang/String;)V > v13,v41 @77 exception:v42(line 90)
BB15
36   return                                  (line 91)
BB16

**CGNode:** Node: < Application, Lorg/apache/catalina/tribes/io/BufferPool, <init>(Lorg/apache/catalina/tribes/io/BufferPool$BufferPoolAPI;)V > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/io/BufferPool, getBufferPool()Lorg/apache/catalina/tribes/io/BufferPool; >:NEW <Application,Lorg/apache/catalina/tribes/io/BufferPool>@136 in ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, main([Ljava/lang/String;)V >:NEW <Application,Lorg/apache/catalina/tribes/io/XByteBuffer>@19 in ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,[Ljava/lang/String>@1 in Everywhere} ]} ]} ]
**IR:** < Application, Lorg/apache/catalina/tribes/io/BufferPool, <init>(Lorg/apache/catalina/tribes/io/BufferPool$BufferPoolAPI;)V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..1]
    -> BB2
    -> BB5
BB2[2..4]
    -> BB3
    -> BB5
BB3[5..7]
    -> BB4
    -> BB5
BB4[8..8]
    -> BB5
BB5[-1..-2]
Instructions:
BB0
BB1
1   invokespecial < Application, Ljava/lang/Object, <init>()V > v1 @1 exception:v4(line 39)
BB2
4   putfield v1 = v5:#null < Application, Lorg/apache/catalina/tribes/io/BufferPool, pool, <Application,Lorg/apache/catalina/tribes/io/BufferPool$BufferPoolAPI> >(line 37)
BB3
7   putfield v1 = v2 < Application, Lorg/apache/catalina/tribes/io/BufferPool, pool, <Application,Lorg/apache/catalina/tribes/io/BufferPool$BufferPoolAPI> >(line 40)
BB4
8   return                                   (line 41)
BB5

**CGNode:** Node: < Application, Lorg/apache/catalina/tribes/io/ChannelData, generateUUID()V > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/io/ChannelData, getDataFromPackage(Lorg/apache/catalina/tribes/io/XByteBuffer;)Lorg/apache/catalina/tribes/io/ChannelData; >:NEW <Application,Lorg/apache/catalina/tribes/io/ChannelData>@0 in ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, main([Ljava/lang/String;)V >:NEW <Application,Lorg/apache/catalina/tribes/io/XByteBuffer>@19 in ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,[Ljava/lang/String>@1 in Everywhere} ]} ]} ]
**IR:** < Application, Lorg/apache/catalina/tribes/io/ChannelData, generateUUID()V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..1]
    -> BB2
    -> BB5
BB2[2..6]
    -> BB3
    -> BB5
BB3[7..10]
    -> BB4
    -> BB5
BB4[11..11]
    -> BB5
BB5[-1..-2]
Instructions:
BB0
BB1
1   v4 = new <Primordial,[B>@2v3:#16         (line 177)
BB2
3   v5 = getstatic < Application, Lorg/apache/catalina/tribes/io/ChannelData, USE_SECURE_RANDOM_FOR_UUID, <Primordial,Z> >(line 178)
6   v8 = invokestatic < Application, Lorg/apache/catalina/tribes/util/UUIDGenerator, randomUUID(Z[BI)[B > v5,v4,v6:#0 @10 exception:v7(line 178)
BB3
10   invokevirtual < Application, Lorg/apache/catalina/tribes/io/ChannelData, setUniqueId([B)V > v1,v4 @16 exception:v9(line 179)
BB4
11   return                                  (line 180)
BB5

**CGNode:** Node: < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, <init>()V > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/membership/MemberImpl, getMember([BII)Lorg/apache/catalina/tribes/membership/MemberImpl; >:NEW <Application,Lorg/apache/catalina/tribes/membership/MemberImpl>@3 in ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, main([Ljava/lang/String;)V >:NEW <Application,Lorg/apache/catalina/tribes/io/XByteBuffer>@19 in ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,[Ljava/lang/String>@1 in Everywhere} ]} ]} ]
**IR:** < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, <init>()V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..1]
    -> BB2
    -> BB16
BB2[2..4]
    -> BB3
    -> BB16
BB3[5..7]
    -> BB4
    -> BB16
BB4[8..10]
    -> BB5
    -> BB16
BB5[11..13]
    -> BB6
    -> BB16
BB6[14..16]
    -> BB7
    -> BB16
BB7[17..19]
    -> BB8
    -> BB16
BB8[20..20]
    -> BB9
    -> BB16
BB9[21..23]
    -> BB10
    -> BB16
BB10[24..24]
    -> BB11
    -> BB16
BB11[25..27]
    -> BB12
    -> BB16
BB12[28..28]
    -> BB13
    -> BB16
BB13[29..31]
    -> BB14
    -> BB16
BB14[32..32]
    -> BB15
    -> BB16
BB15[33..33]
    -> BB16
BB16[-1..-2]
Instructions:
BB0
BB1
1   invokespecial < Application, Ljava/lang/Object, <init>()V > v1 @1 exception:v3(line 119)
BB2
4   putfield v1 = v4:#-1 < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, udpPort, <Primordial,I> >(line 66)
BB3
7   putfield v1 = v4:#-1 < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, securePort, <Primordial,I> >(line 71)
BB4
10   putfield v1 = v5:#0 < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, msgCount, <Primordial,I> >(line 76)
BB5
13   putfield v1 = v6:#0 < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, memberAliveTime, <Primordial,J> >(line 81)
BB6
16   putfield v1 = v7:#null < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, dataPkg, <Primordial,[B> >(line 92)
BB7
19   v9 = new <Primordial,[B>@32v8:#16       (line 97)
BB8
20   putfield v1 = v9 < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, uniqueId, <Primordial,[B> >(line 97)
BB9
23   v10 = new <Primordial,[B>@39v5:#0       (line 103)
BB10
24   putfield v1 = v10 < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, payload, <Primordial,[B> >(line 103)
BB11
27   v11 = new <Primordial,[B>@46v5:#0       (line 109)
BB12
28   putfield v1 = v11 < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, command, <Primordial,[B> >(line 109)
BB13
31   v12 = new <Primordial,[B>@53v5:#0       (line 114)
BB14
32   putfield v1 = v12 < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, domain, <Primordial,[B> >(line 114)
BB15
33   return                                  (line 121)
BB16

**CGNode:** Node: < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, getMember([BIILorg/apache/catalina/tribes/membership/MemberImpl;)Lorg/apache/catalina/tribes/membership/MemberImpl; > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, main([Ljava/lang/String;)V >:NEW <Application,Lorg/apache/catalina/tribes/io/XByteBuffer>@19 in ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,[Ljava/lang/String>@1 in Everywhere} ]} ]
**IR:** < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, getMember([BIILorg/apache/catalina/tribes/membership/MemberImpl;)Lorg/apache/catalina/tribes/membership/MemberImpl; >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..5]
    -> BB2
    -> BB80
BB2[6..7]
    -> BB11
    -> BB3
BB3[8..8]
    -> BB4
    -> BB80
BB4[9..10]
    -> BB5
    -> BB80
BB5[11..13]
    -> BB6
    -> BB80
BB6[14..15]
    -> BB7
    -> BB80
BB7[16..16]
    -> BB8
    -> BB80
BB8[17..17]
    -> BB9
    -> BB80
BB9[18..18]
    -> BB10
    -> BB80
BB10[19..19]
    -> BB80
BB11[20..22]
    -> BB12
    -> BB80
BB12[23..25]
    -> BB16
    -> BB13
BB13[26..26]
    -> BB14
    -> BB80
BB14[27..29]
    -> BB15
    -> BB80
BB15[30..30]
    -> BB80
BB16[31..33]
    -> BB17
    -> BB80
BB17[34..38]
    -> BB18
    -> BB80
BB18[39..49]
    -> BB19
    -> BB80
BB19[50..52]
    -> BB20
    -> BB80
BB20[53..54]
    -> BB24
    -> BB21
BB21[55..55]
    -> BB22
    -> BB80
BB22[56..58]
    -> BB23
    -> BB80
BB23[59..59]
    -> BB80
BB24[60..67]
    -> BB25
    -> BB80
BB25[68..69]
    -> BB34
    -> BB26
BB26[70..70]
    -> BB27
    -> BB80
BB27[71..72]
    -> BB28
    -> BB80
BB28[73..75]
    -> BB29
    -> BB80
BB29[76..77]
    -> BB30
    -> BB80
BB30[78..78]
    -> BB31
    -> BB80
BB31[79..79]
    -> BB32
    -> BB80
BB32[80..80]
    -> BB33
    -> BB80
BB33[81..81]
    -> BB80
BB34[82..83]
    -> BB35
    -> BB80
BB35[84..90]
    -> BB36
    -> BB80
BB36[91..96]
    -> BB37
    -> BB80
BB37[97..103]
    -> BB38
    -> BB80
BB38[104..109]
    -> BB39
    -> BB80
BB39[110..116]
    -> BB40
    -> BB80
BB40[117..122]
    -> BB41
    -> BB80
BB41[123..129]
    -> BB42
    -> BB80
BB42[130..140]
    -> BB43
    -> BB80
BB43[141..143]
    -> BB44
    -> BB80
BB44[144..150]
    -> BB45
    -> BB80
BB45[151..157]
    -> BB46
    -> BB80
BB46[158..164]
    -> BB47
    -> BB80
BB47[165..171]
    -> BB48
    -> BB80
BB48[172..172]
    -> BB49
    -> BB80
BB49[173..175]
    -> BB50
    -> BB80
BB50[176..180]
    -> BB51
    -> BB80
BB51[181..187]
    -> BB52
    -> BB80
BB52[188..194]
    -> BB53
    -> BB80
BB53[195..195]
    -> BB54
    -> BB80
BB54[196..198]
    -> BB55
    -> BB80
BB55[199..202]
    -> BB56
    -> BB80
BB56[203..209]
    -> BB57
    -> BB80
BB57[210..216]
    -> BB58
    -> BB80
BB58[217..223]
    -> BB59
    -> BB80
BB59[224..230]
    -> BB60
    -> BB80
BB60[231..231]
    -> BB61
    -> BB80
BB61[232..234]
    -> BB62
    -> BB80
BB62[235..239]
    -> BB63
    -> BB80
BB63[240..243]
    -> BB64
    -> BB80
BB64[244..244]
    -> BB65
    -> BB80
BB65[245..248]
    -> BB66
    -> BB80
BB66[249..249]
    -> BB67
    -> BB80
BB67[250..253]
    -> BB68
    -> BB80
BB68[254..254]
    -> BB69
    -> BB80
BB69[255..258]
    -> BB70
    -> BB80
BB70[259..259]
    -> BB71
    -> BB80
BB71[260..262]
    -> BB72
    -> BB80
BB72[263..265]
    -> BB73
    -> BB80
BB73[266..268]
    -> BB74
    -> BB80
BB74[269..271]
    -> BB75
    -> BB80
BB75[272..274]
    -> BB76
    -> BB80
BB76[275..275]
    -> BB77
    -> BB80
BB77[276..279]
    -> BB78
    -> BB80
BB78[280..282]
    -> BB79
    -> BB80
BB79[283..284]
    -> BB80
BB80[-1..-2]
Instructions:
BB0
BB1
4   v6 = getstatic < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, TRIBES_MBR_BEGIN, <Primordial,[B> >(line 332)
5   v8 = invokestatic < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, firstIndexOf([BI[B)I > v1,v2,v6 @8 exception:v7(line 332)
BB2
7   conditional branch(eq) v8,v2             (line 332)
BB3
8   v113 = new <Application,Ljava/lang/IllegalArgumentException>@16(line 333)
BB4
10   v114 = new <Application,Ljava/lang/StringBuilder>@20(line 333)
BB5
13   invokespecial < Application, Ljava/lang/StringBuilder, <init>(Ljava/lang/String;)V > v114,v115:#Invalid package, should start with: @26 exception:v116(line 333)
BB6
14   v117 = getstatic < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, TRIBES_MBR_BEGIN, <Primordial,[B> >(line 333)
15   v119 = invokestatic < Application, Lorg/apache/catalina/tribes/util/Arrays, toString([B)Ljava/lang/String; > v117 @32 exception:v118(line 333)
BB7
16   v121 = invokevirtual < Application, Ljava/lang/StringBuilder, append(Ljava/lang/String;)Ljava/lang/StringBuilder; > v114,v119 @35 exception:v120(line 333)
BB8
17   v123 = invokevirtual < Application, Ljava/lang/StringBuilder, toString()Ljava/lang/String; > v121 @38 exception:v122(line 333)
BB9
18   invokespecial < Application, Ljava/lang/IllegalArgumentException, <init>(Ljava/lang/String;)V > v113,v123 @41 exception:v124(line 333)
BB10
19   throw v113                              (line 333)
BB11
21   v9 = getstatic < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, TRIBES_MBR_BEGIN, <Primordial,[B> >(line 336)
22   v10 = arraylength v9                    (line 336)
BB12
24   v12 = binaryop(add) v10 , v11:#4        (line 336)
25   conditional branch(ge) v3,v12           (line 336)
BB13
26   v110 = new <Application,Ljava/lang/ArrayIndexOutOfBoundsException>@55(line 337)
BB14
29   invokespecial < Application, Ljava/lang/ArrayIndexOutOfBoundsException, <init>(Ljava/lang/String;)V > v110,v111:#Member package to small to validate. @61 exception:v112(line 337)
BB15
30   throw v110                              (line 337)
BB16
32   v13 = getstatic < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, TRIBES_MBR_BEGIN, <Primordial,[B> >(line 340)
33   v14 = arraylength v13                   (line 340)
BB17
34   v15 = binaryop(add) v2 , v14            (line 340)
38   v17 = invokestatic < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, toInt([BI)I > v1,v15 @77 exception:v16(line 342)
BB18
42   v18 = binaryop(add) v15 , v11:#4        (line 343)
47   v19 = binaryop(add) v17 , v11:#4        (line 345)
48   v20 = getstatic < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, TRIBES_MBR_BEGIN, <Primordial,[B> >(line 345)
49   v21 = arraylength v20                   (line 345)
BB19
50   v22 = binaryop(add) v19 , v21           (line 345)
51   v23 = getstatic < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, TRIBES_MBR_END, <Primordial,[B> >(line 345)
52   v24 = arraylength v23                   (line 345)
BB20
53   v25 = binaryop(add) v22 , v24           (line 345)
54   conditional branch(ge) v3,v25           (line 345)
BB21
55   v107 = new <Application,Ljava/lang/ArrayIndexOutOfBoundsException>@103(line 346)
BB22
58   invokespecial < Application, Ljava/lang/ArrayIndexOutOfBoundsException, <init>(Ljava/lang/String;)V > v107,v108:#Not enough bytes in member package. @109 exception:v109(line 346)
BB23
59   throw v107                              (line 346)
BB24
62   v26 = binaryop(add) v18 , v17           (line 349)
66   v27 = getstatic < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, TRIBES_MBR_END, <Primordial,[B> >(line 350)
67   v29 = invokestatic < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, firstIndexOf([BI[B)I > v1,v26,v27 @126 exception:v28(line 350)
BB25
69   conditional branch(eq) v29,v26          (line 350)
BB26
70   v95 = new <Application,Ljava/lang/IllegalArgumentException>@134(line 351)
BB27
72   v96 = new <Application,Ljava/lang/StringBuilder>@138(line 351)
BB28
75   invokespecial < Application, Ljava/lang/StringBuilder, <init>(Ljava/lang/String;)V > v96,v97:#Invalid package, should end with: @144 exception:v98(line 351)
BB29
76   v99 = getstatic < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, TRIBES_MBR_END, <Primordial,[B> >(line 351)
77   v101 = invokestatic < Application, Lorg/apache/catalina/tribes/util/Arrays, toString([B)Ljava/lang/String; > v99 @150 exception:v100(line 351)
BB30
78   v103 = invokevirtual < Application, Ljava/lang/StringBuilder, append(Ljava/lang/String;)Ljava/lang/StringBuilder; > v96,v101 @153 exception:v102(line 351)
BB31
79   v105 = invokevirtual < Application, Ljava/lang/StringBuilder, toString()Ljava/lang/String; > v103 @156 exception:v104(line 351)
BB32
80   invokespecial < Application, Ljava/lang/IllegalArgumentException, <init>(Ljava/lang/String;)V > v95,v105 @159 exception:v106(line 351)
BB33
81   throw v95                               (line 351)
BB34
83   v31 = new <Primordial,[B>@165v30:#8     (line 355)
BB35
90   invokestatic < Application, Ljava/lang/System, arraycopy(Ljava/lang/Object;ILjava/lang/Object;II)V > v1,v18,v31,v32:#0,v30:#8 @177 exception:v33(line 356)
BB36
93   v34 = binaryop(add) v18 , v30:#8        (line 357)
96   v35 = new <Primordial,[B>@184v11:#4     (line 358)
BB37
103   invokestatic < Application, Ljava/lang/System, arraycopy(Ljava/lang/Object;ILjava/lang/Object;II)V > v1,v34,v35,v32:#0,v11:#4 @195 exception:v36(line 359)
BB38
106   v37 = binaryop(add) v34 , v11:#4       (line 360)
109   v38 = new <Primordial,[B>@202v11:#4    (line 362)
BB39
116   invokestatic < Application, Ljava/lang/System, arraycopy(Ljava/lang/Object;ILjava/lang/Object;II)V > v1,v37,v38,v32:#0,v11:#4 @213 exception:v39(line 363)
BB40
119   v40 = binaryop(add) v37 , v11:#4       (line 364)
122   v41 = new <Primordial,[B>@220v11:#4    (line 366)
BB41
129   invokestatic < Application, Ljava/lang/System, arraycopy(Ljava/lang/Object;ILjava/lang/Object;II)V > v1,v40,v41,v32:#0,v11:#4 @231 exception:v42(line 367)
BB42
132   v43 = binaryop(add) v40 , v11:#4       (line 368)
138   v45 = binaryop(add) v43 , v44:#1       (line 371)
140   v46 = arrayload v1[v43]                (line 371)
BB43
143   v47 = new <Primordial,[B>@248v46       (line 372)
BB44
150   invokestatic < Application, Ljava/lang/System, arraycopy(Ljava/lang/Object;ILjava/lang/Object;II)V > v1,v45,v47,v32:#0,v46 @260 exception:v48(line 373)
BB45
153   v49 = binaryop(add) v45 , v46          (line 374)
157   v51 = invokestatic < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, toInt([BI)I > v1,v49 @273 exception:v50(line 376)
BB46
161   v52 = binaryop(add) v49 , v11:#4       (line 377)
164   v53 = new <Primordial,[B>@283v51       (line 379)
BB47
171   v54 = arraylength v53                  (line 380)
BB48
172   invokestatic < Application, Ljava/lang/System, arraycopy(Ljava/lang/Object;ILjava/lang/Object;II)V > v1,v52,v53,v32:#0,v54 @296 exception:v55(line 380)
BB49
175   v56 = arraylength v53                  (line 381)
BB50
176   v57 = binaryop(add) v52 , v56          (line 381)
180   v59 = invokestatic < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, toInt([BI)I > v1,v57 @310 exception:v58(line 383)
BB51
184   v60 = binaryop(add) v57 , v11:#4       (line 384)
187   v61 = new <Primordial,[B>@320v59       (line 386)
BB52
194   v62 = arraylength v61                  (line 387)
BB53
195   invokestatic < Application, Ljava/lang/System, arraycopy(Ljava/lang/Object;ILjava/lang/Object;II)V > v1,v60,v61,v32:#0,v62 @333 exception:v63(line 387)
BB54
198   v64 = arraylength v61                  (line 388)
BB55
199   v65 = binaryop(add) v60 , v64          (line 388)
202   v67 = new <Primordial,[B>@346v66:#16   (line 390)
BB56
209   invokestatic < Application, Ljava/lang/System, arraycopy(Ljava/lang/Object;ILjava/lang/Object;II)V > v1,v65,v67,v32:#0,v66:#16 @358 exception:v68(line 391)
BB57
212   v69 = binaryop(add) v65 , v66:#16      (line 392)
216   v71 = invokestatic < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, toInt([BI)I > v1,v69 @367 exception:v70(line 394)
BB58
220   v72 = binaryop(add) v69 , v11:#4       (line 395)
223   v73 = new <Primordial,[B>@377v71       (line 397)
BB59
230   v74 = arraylength v73                  (line 398)
BB60
231   invokestatic < Application, Ljava/lang/System, arraycopy(Ljava/lang/Object;ILjava/lang/Object;II)V > v1,v72,v73,v32:#0,v74 @390 exception:v75(line 398)
BB61
234   v76 = arraylength v73                  (line 399)
BB62
235   v77 = binaryop(add) v72 , v76          (line 399)
239   invokevirtual < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, setHost([B)V > v4,v47 @404 exception:v78(line 401)
BB63
243   v80 = invokestatic < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, toInt([BI)I > v35,v32:#0 @411 exception:v79(line 402)
BB64
244   invokevirtual < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, setPort(I)V > v4,v80 @414 exception:v81(line 402)
BB65
248   v83 = invokestatic < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, toInt([BI)I > v38,v32:#0 @421 exception:v82(line 403)
BB66
249   invokevirtual < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, setSecurePort(I)V > v4,v83 @424 exception:v84(line 403)
BB67
253   v86 = invokestatic < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, toInt([BI)I > v41,v32:#0 @431 exception:v85(line 404)
BB68
254   invokevirtual < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, setUdpPort(I)V > v4,v86 @434 exception:v87(line 404)
BB69
258   v89 = invokestatic < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, toLong([BI)J > v31,v32:#0 @441 exception:v88(line 405)
BB70
259   invokevirtual < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, setMemberAliveTime(J)V > v4,v89 @444 exception:v90(line 405)
BB71
262   invokevirtual < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, setUniqueId([B)V > v4,v67 @450 exception:v91(line 406)
BB72
265   putfield v4 = v73 < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, payload, <Primordial,[B> >(line 407)
BB73
268   putfield v4 = v61 < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, domain, <Primordial,[B> >(line 408)
BB74
271   putfield v4 = v53 < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, command, <Primordial,[B> >(line 409)
BB75
274   v92 = new <Primordial,[B>@473v3        (line 411)
BB76
275   putfield v4 = v92 < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, dataPkg, <Primordial,[B> >(line 411)
BB77
279   v93 = getfield < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, dataPkg, <Primordial,[B> > v4(line 412)
BB78
282   invokestatic < Application, Ljava/lang/System, arraycopy(Ljava/lang/Object;ILjava/lang/Object;II)V > v1,v2,v93,v32:#0,v3 @486 exception:v94(line 412)
BB79
284   return v4                              (line 414)
BB80

**CGNode:** Node: < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint$BindState, <init>(Ljava/lang/String;I)V > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/tomcat/util/net/AbstractEndpoint$BindState, <clinit>()V >:NEW <Application,Lorg/apache/tomcat/util/net/AbstractEndpoint$BindState>@0 in Everywhere} ]
**IR:** < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint$BindState, <init>(Ljava/lang/String;I)V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..3]
    -> BB2
    -> BB3
BB2[4..4]
    -> BB3
BB3[-1..-2]
Instructions:
BB0
BB1
3   invokespecial < Application, Ljava/lang/Enum, <init>(Ljava/lang/String;I)V > v1,v2,v3 @3 exception:v5(line 76)
BB2
4   return                                   (line 76)
BB3

**CGNode:** Node: < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint$BindState, <init>(Ljava/lang/String;I)V > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/tomcat/util/net/AbstractEndpoint$BindState, <clinit>()V >:NEW <Application,Lorg/apache/tomcat/util/net/AbstractEndpoint$BindState>@13 in Everywhere} ]
**IR:** < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint$BindState, <init>(Ljava/lang/String;I)V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..3]
    -> BB2
    -> BB3
BB2[4..4]
    -> BB3
BB3[-1..-2]
Instructions:
BB0
BB1
3   invokespecial < Application, Ljava/lang/Enum, <init>(Ljava/lang/String;I)V > v1,v2,v3 @3 exception:v5(line 76)
BB2
4   return                                   (line 76)
BB3

**CGNode:** Node: < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint$BindState, <init>(Ljava/lang/String;I)V > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/tomcat/util/net/AbstractEndpoint$BindState, <clinit>()V >:NEW <Application,Lorg/apache/tomcat/util/net/AbstractEndpoint$BindState>@26 in Everywhere} ]
**IR:** < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint$BindState, <init>(Ljava/lang/String;I)V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..3]
    -> BB2
    -> BB3
BB2[4..4]
    -> BB3
BB3[-1..-2]
Instructions:
BB0
BB1
3   invokespecial < Application, Ljava/lang/Enum, <init>(Ljava/lang/String;I)V > v1,v2,v3 @3 exception:v5(line 76)
BB2
4   return                                   (line 76)
BB3

**CGNode:** Node: < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint$Acceptor, <init>()V > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/tomcat/util/net/AprEndpoint, createAcceptor()Lorg/apache/tomcat/util/net/AbstractEndpoint$Acceptor; >:NEW <Application,Lorg/apache/tomcat/util/net/AprEndpoint$Acceptor>@0 in ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, main([Ljava/lang/String;)V >:NEW <Application,Lorg/apache/tomcat/util/net/AprEndpoint>@0 in ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,[Ljava/lang/String>@6 in Everywhere} ]} ]} ]
**IR:** < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint$Acceptor, <init>()V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..1]
    -> BB2
    -> BB4
BB2[2..4]
    -> BB3
    -> BB4
BB3[5..5]
    -> BB4
BB4[-1..-2]
Instructions:
BB0
BB1
1   invokespecial < Application, Ljava/lang/Object, <init>()V > v1 @1 exception:v3(line 80)
BB2
3   v4 = getstatic < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint$Acceptor$AcceptorState, NEW, <Application,Lorg/apache/tomcat/util/net/AbstractEndpoint$Acceptor$AcceptorState> >(line 85)
4   putfield v1 = v4 < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint$Acceptor, state, <Application,Lorg/apache/tomcat/util/net/AbstractEndpoint$Acceptor$AcceptorState> >(line 85)
BB3
5   return                                   (line 80)
BB4

**CGNode:** Node: < Application, Lorg/apache/catalina/tribes/util/UUIDGenerator, randomUUID(Z[BI)[B > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/io/ChannelData, getDataFromPackage(Lorg/apache/catalina/tribes/io/XByteBuffer;)Lorg/apache/catalina/tribes/io/ChannelData; >:NEW <Application,Lorg/apache/catalina/tribes/io/ChannelData>@0 in ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, main([Ljava/lang/String;)V >:NEW <Application,Lorg/apache/catalina/tribes/io/XByteBuffer>@19 in ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,[Ljava/lang/String>@1 in Everywhere} ]} ]} ]
**IR:** < Application, Lorg/apache/catalina/tribes/util/UUIDGenerator, randomUUID(Z[BI)[B >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..4]
    -> BB2
    -> BB27
BB2[5..5]
    -> BB13
    -> BB3
BB3[6..6]
    -> BB4
    -> BB27
BB4[7..8]
    -> BB5
    -> BB27
BB5[9..11]
    -> BB6
    -> BB27
BB6[12..13]
    -> BB7
    -> BB27
BB7[14..14]
    -> BB8
    -> BB27
BB8[15..16]
    -> BB9
    -> BB27
BB9[17..20]
    -> BB10
    -> BB27
BB10[21..21]
    -> BB11
    -> BB27
BB11[22..22]
    -> BB12
    -> BB27
BB12[23..23]
    -> BB27
BB13[24..26]
    -> BB16
    -> BB14
BB14[27..29]
    -> BB16
    -> BB15
BB15[30..31]
    -> BB17
BB16[32..32]
    -> BB17
BB17[33..38]
    -> BB18
    -> BB27
BB18[39..44]
    -> BB19
    -> BB27
BB19[45..48]
    -> BB20
    -> BB27
BB20[49..54]
    -> BB21
    -> BB27
BB21[55..58]
    -> BB22
    -> BB27
BB22[59..64]
    -> BB23
    -> BB27
BB23[65..68]
    -> BB24
    -> BB27
BB24[69..74]
    -> BB25
    -> BB27
BB25[75..78]
    -> BB26
    -> BB27
BB26[79..80]
    -> BB27
BB27[-1..-2]
Instructions:
BB0
BB1
2   v6 = binaryop(add) v3 , v5:#16           (line 61)
4   v7 = arraylength v2                      (line 61)
BB2
5   conditional branch(le) v6,v7             (line 61)
BB3
6   v37 = new <Application,Ljava/lang/ArrayIndexOutOfBoundsException>@9(line 62)
BB4
8   v38 = new <Application,Ljava/lang/StringBuilder>@13(line 62)
BB5
11   invokespecial < Application, Ljava/lang/StringBuilder, <init>(Ljava/lang/String;)V > v38,v39:#Unable to fit 16 bytes into the array. length: @19 exception:v40(line 62)
BB6
13   v41 = arraylength v2                    (line 62)
BB7
14   v43 = invokevirtual < Application, Ljava/lang/StringBuilder, append(I)Ljava/lang/StringBuilder; > v38,v41 @24 exception:v42(line 62)
BB8
16   v46 = invokevirtual < Application, Ljava/lang/StringBuilder, append(Ljava/lang/String;)Ljava/lang/StringBuilder; > v43,v44:# required length: @29 exception:v45(line 62)
BB9
19   v47 = binaryop(add) v3 , v5:#16         (line 62)
20   v49 = invokevirtual < Application, Ljava/lang/StringBuilder, append(I)Ljava/lang/StringBuilder; > v46,v47 @36 exception:v48(line 62)
BB10
21   v51 = invokevirtual < Application, Ljava/lang/StringBuilder, toString()Ljava/lang/String; > v49 @39 exception:v50(line 62)
BB11
22   invokespecial < Application, Ljava/lang/ArrayIndexOutOfBoundsException, <init>(Ljava/lang/String;)V > v37,v51 @42 exception:v52(line 62)
BB12
23   throw v37                               (line 62)
BB13
26   conditional branch(eq) v1,v8:#0         (line 63)
BB14
27   v9 = getstatic < Application, Lorg/apache/catalina/tribes/util/UUIDGenerator, secrand, <Application,Ljava/security/SecureRandom> >(line 63)
29   conditional branch(eq) v9,v10:#null     (line 63)
BB15
30   v12 = getstatic < Application, Lorg/apache/catalina/tribes/util/UUIDGenerator, secrand, <Application,Ljava/security/SecureRandom> >(line 63)
31   goto                                    (line 63)
BB16
32   v11 = getstatic < Application, Lorg/apache/catalina/tribes/util/UUIDGenerator, rand, <Application,Ljava/util/Random> >(line 63)
BB17
           v13 = phi  v12,v11
38   invokestatic < Application, Lorg/apache/catalina/tribes/util/UUIDGenerator, nextBytes([BIILjava/util/Random;)V > v2,v3,v5:#16,v13 @71 exception:v14(line 64)
BB18
42   v16 = binaryop(add) v15:#6 , v3         (line 65)
44   v17 = arrayload v2[v16]                 (line 65)
BB19
46   v19 = binaryop(and) v17 , v18:#15       (line 65)
47   v20 = conversion(B) v19                 (line 65)
48   arraystore v2[v16] = v20                (line 65)
BB20
52   v21 = binaryop(add) v15:#6 , v3         (line 66)
54   v22 = arrayload v2[v21]                 (line 66)
BB21
56   v24 = binaryop(or) v22 , v23:#64        (line 66)
57   v25 = conversion(B) v24                 (line 66)
58   arraystore v2[v21] = v25                (line 66)
BB22
62   v27 = binaryop(add) v26:#8 , v3         (line 67)
64   v28 = arrayload v2[v27]                 (line 67)
BB23
66   v30 = binaryop(and) v28 , v29:#63       (line 67)
67   v31 = conversion(B) v30                 (line 67)
68   arraystore v2[v27] = v31                (line 67)
BB24
72   v32 = binaryop(add) v26:#8 , v3         (line 68)
74   v33 = arrayload v2[v32]                 (line 68)
BB25
76   v35 = binaryop(or) v33 , v34:#128       (line 68)
77   v36 = conversion(B) v35                 (line 68)
78   arraystore v2[v32] = v36                (line 68)
BB26
80   return v2                               (line 69)
BB27

**CGNode:** Node: < Application, Lorg/apache/catalina/tribes/util/UUIDGenerator, <clinit>()V > Context: Everywhere
**IR:** < Application, Lorg/apache/catalina/tribes/util/UUIDGenerator, <clinit>()V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..0]
    -> BB2
    -> BB20
BB2[1..1]
    -> BB3
    -> BB20
BB3[2..4]
    -> BB4
    -> BB20
BB4[5..8]
    -> BB5
    -> BB20
BB5[9..10]
    -> BB6
    -> BB20
BB6[11..12]
    -> BB7
    -> BB20
BB7[13..14]
    -> BB8
    -> BB20
BB8[15..16]
    -> BB9
    -> BB20
BB9[17..19]
    -> BB10
    -> BB20
BB10[20..21]
    -> BB11
    -> BB20
BB11[22..29]
    -> BB19
    -> BB12
BB12[30..34]
    -> BB13
    -> BB20
BB13[35..38]
    -> BB14
    -> BB20
BB14[39..39]
    -> BB15
    -> BB20
BB15[40..43]
    -> BB16
    -> BB20
BB16[44..44]
    -> BB17
    -> BB20
BB17[45..45]
    -> BB18
    -> BB20
BB18[46..46]
    -> BB19
    -> BB20
BB19[47..47]
    -> BB20
BB20[-1..-2]
Instructions:
BB0
BB1
0   v2 = load_metadata: <Primordial,Lorg/apache/catalina/tribes/util/UUIDGenerator>, <Primordial,Ljava/lang/Class>(line 31)
BB2
1   v4 = invokestatic < Application, Lorg/apache/juli/logging/LogFactory, getLog(Ljava/lang/Class;)Lorg/apache/juli/logging/Log; > v2 @2 exception:v3(line 31)
BB3
2   putstatic v4 < Application, Lorg/apache/catalina/tribes/util/UUIDGenerator, log, <Application,Lorg/apache/juli/logging/Log> >(line 31)
4   v7 = invokestatic < Application, Lorg/apache/catalina/tribes/util/StringManager, getManager(Ljava/lang/String;)Lorg/apache/catalina/tribes/util/StringManager; > v5:#org.apache.catalina.tribes.util @10 exception:v6(line 33)
BB4
5   putstatic v7 < Application, Lorg/apache/catalina/tribes/util/UUIDGenerator, sm, <Application,Lorg/apache/catalina/tribes/util/StringManager> >(line 32)
7   putstatic v8:#null < Application, Lorg/apache/catalina/tribes/util/UUIDGenerator, secrand, <Application,Ljava/security/SecureRandom> >(line 40)
8   v9 = new <Application,Ljava/util/Random>@20(line 41)
BB5
10   invokespecial < Application, Ljava/util/Random, <init>()V > v9 @24 exception:v10(line 41)
BB6
11   putstatic v9 < Application, Lorg/apache/catalina/tribes/util/UUIDGenerator, rand, <Application,Ljava/util/Random> >(line 41)
12   v12 = invokestatic < Application, Ljava/lang/System, currentTimeMillis()J > @30 exception:v11(line 44)
BB7
14   v13 = new <Application,Ljava/security/SecureRandom>@34(line 45)
BB8
16   invokespecial < Application, Ljava/security/SecureRandom, <init>()V > v13 @38 exception:v14(line 45)
BB9
17   putstatic v13 < Application, Lorg/apache/catalina/tribes/util/UUIDGenerator, secrand, <Application,Ljava/security/SecureRandom> >(line 45)
18   v15 = getstatic < Application, Lorg/apache/catalina/tribes/util/UUIDGenerator, secrand, <Application,Ljava/security/SecureRandom> >(line 47)
19   v17 = invokevirtual < Application, Ljava/security/SecureRandom, nextInt()I > v15 @47 exception:v16(line 47)
BB10
21   v19 = invokestatic < Application, Ljava/lang/System, currentTimeMillis()J > @51 exception:v18(line 48)
BB11
23   v20 = binaryop(sub) v19 , v12           (line 48)
27   v22 = compare v20,v21:#100 opcode=cmp   (line 49)
29   conditional branch(le) v22,v23:#0       (line 49)
BB12
30   v24 = getstatic < Application, Lorg/apache/catalina/tribes/util/UUIDGenerator, log, <Application,Lorg/apache/juli/logging/Log> >(line 50)
31   v25 = getstatic < Application, Lorg/apache/catalina/tribes/util/UUIDGenerator, sm, <Application,Lorg/apache/catalina/tribes/util/StringManager> >(line 50)
34   v28 = new <Application,[Ljava/lang/Object>@74v27:#2 (line 50)
BB13
37   v29 = getstatic < Application, Lorg/apache/catalina/tribes/util/UUIDGenerator, secrand, <Application,Ljava/security/SecureRandom> >(line 51)
38   v31 = invokevirtual < Application, Ljava/security/SecureRandom, getAlgorithm()Ljava/lang/String; > v29 @82 exception:v30(line 51)
BB14
39   arraystore v28[v23:#0] = v31            (line 51)
BB15
43   v34 = invokestatic < Application, Ljava/lang/Long, valueOf(J)Ljava/lang/Long; > v20 @89 exception:v33(line 51)
BB16
44   arraystore v28[v32:#1] = v34            (line 51)
BB17
45   v36 = invokevirtual < Application, Lorg/apache/catalina/tribes/util/StringManager, getString(Ljava/lang/String;[Ljava/lang/Object;)Ljava/lang/String; > v25,v26:#uuidGenerator.createRandom,v28 @93 exception:v35(line 50)
BB18
46   invokeinterface < Application, Lorg/apache/juli/logging/Log, info(Ljava/lang/Object;)V > v24,v36 @96 exception:v37(line 50)
BB19
47   return                                  (line 30)
BB20

**CGNode:** Node: < Application, Lorg/apache/catalina/tribes/io/ChannelData, setUniqueId([B)V > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/io/ChannelData, getDataFromPackage(Lorg/apache/catalina/tribes/io/XByteBuffer;)Lorg/apache/catalina/tribes/io/ChannelData; >:NEW <Application,Lorg/apache/catalina/tribes/io/ChannelData>@0 in ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, main([Ljava/lang/String;)V >:NEW <Application,Lorg/apache/catalina/tribes/io/XByteBuffer>@19 in ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,[Ljava/lang/String>@1 in Everywhere} ]} ]} ]
**IR:** < Application, Lorg/apache/catalina/tribes/io/ChannelData, setUniqueId([B)V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..2]
    -> BB2
    -> BB3
BB2[3..3]
    -> BB3
BB3[-1..-2]
Instructions:
BB0
BB1
2   putfield v1 = v2 < Application, Lorg/apache/catalina/tribes/io/ChannelData, uniqueId, <Primordial,[B> >(line 134)
BB2
3   return                                   (line 135)
BB3

**CGNode:** Node: < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, firstIndexOf([BI[B)I > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, main([Ljava/lang/String;)V >:NEW <Application,Lorg/apache/catalina/tribes/io/XByteBuffer>@19 in ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,[Ljava/lang/String>@1 in Everywhere} ]} ]
**IR:** < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, firstIndexOf([BI[B)I >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..3]
    -> BB2
    -> BB45
BB2[4..5]
    -> BB3
    -> BB45
BB3[6..6]
    -> BB5
    -> BB4
BB4[7..8]
    -> BB45
BB5[9..10]
    -> BB6
    -> BB45
BB6[11..12]
    -> BB9
    -> BB7
BB7[13..14]
    -> BB8
    -> BB45
BB8[15..16]
    -> BB10
    -> BB9
BB9[17..18]
    -> BB45
BB10[19..21]
    -> BB11
    -> BB45
BB11[22..22]
    -> BB15
    -> BB12
BB12[23..23]
    -> BB13
    -> BB45
BB13[24..25]
    -> BB14
    -> BB45
BB14[26..26]
    -> BB45
BB15[27..30]
    -> BB16
    -> BB45
BB16[31..33]
    -> BB17
    -> BB45
BB17[34..37]
    -> BB18
    -> BB45
BB18[38..41]
    -> BB43
BB19[42..45]
    -> BB20
    -> BB45
BB20[46..46]
    -> BB22
    -> BB21
BB21[47..47]
    -> BB24
BB22[48..51]
    -> BB23
BB23[52..54]
    -> BB19
    -> BB24
BB24[55..57]
    -> BB26
    -> BB25
BB25[58..59]
    -> BB45
BB26[60..64]
    -> BB28
    -> BB27
BB27[65..66]
    -> BB45
BB28[67..71]
    -> BB36
BB29[72..74]
    -> BB34
    -> BB30
BB30[75..77]
    -> BB31
    -> BB45
BB31[78..82]
    -> BB32
    -> BB45
BB32[83..83]
    -> BB34
    -> BB33
BB33[84..85]
    -> BB35
BB34[86..86]
    -> BB35
BB35[87..91]
    -> BB36
BB36[92..94]
    -> BB38
    -> BB37
BB37[95..97]
    -> BB29
    -> BB38
BB38[98..100]
    -> BB40
    -> BB39
BB39[101..103]
    -> BB43
BB40[104..108]
    -> BB42
    -> BB41
BB41[109..110]
    -> BB45
BB42[111..114]
    -> BB43
BB43[115..117]
    -> BB23
    -> BB44
BB44[118..119]
    -> BB45
BB45[-1..-2]
Instructions:
BB0
BB1
3   v6 = arraylength v3                      (line 510)
BB2
5   v7 = arraylength v1                      (line 510)
BB3
6   conditional branch(le) v6,v7             (line 510)
BB4
8   return v5:#-1                            (line 510)
BB5
10   v8 = arraylength v3                     (line 511)
BB6
12   conditional branch(eq) v8,v9:#0         (line 511)
BB7
14   v10 = arraylength v1                    (line 511)
BB8
16   conditional branch(ne) v10,v9:#0        (line 511)
BB9
18   return v5:#-1                           (line 511)
BB10
21   v11 = arraylength v1                    (line 512)
BB11
22   conditional branch(lt) v2,v11           (line 512)
BB12
23   v35 = new <Application,Ljava/lang/ArrayIndexOutOfBoundsException>@29(line 512)
BB13
25   invokespecial < Application, Ljava/lang/ArrayIndexOutOfBoundsException, <init>()V > v35 @33 exception:v36(line 512)
BB14
26   throw v35                               (line 512)
BB15
30   v12 = arraylength v1                    (line 514)
BB16
33   v13 = arraylength v3                    (line 515)
BB17
37   v14 = arrayload v3[v9:#0]               (line 516)
BB18
41   goto                                    (line 518)
BB19
45   v15 = arrayload v1[v18]                 (line 521)
BB20
46   conditional branch(ne) v14,v15          (line 521)
BB21
47   goto                                    (line 522)
BB22
50   v17 = binaryop(add) v18 , v16:#1        (line 523)
BB23
           v30 = phi  v27,v30
           v18 = phi  v29,v17
54   conditional branch(lt) v18,v12          (line 520)
BB24
57   conditional branch(lt) v18,v12          (line 525)
BB25
59   return v5:#-1                           (line 526)
BB26
62   v19 = binaryop(sub) v12 , v18           (line 530)
64   conditional branch(ge) v19,v13          (line 530)
BB27
66   return v5:#-1                           (line 531)
BB28
71   goto                                    (line 534)
BB29
74   conditional branch(eq) v25,v9:#0        (line 535)
BB30
77   v20 = arrayload v3[v26]                 (line 535)
BB31
81   v21 = binaryop(add) v18 , v26           (line 535)
82   v22 = arrayload v1[v21]                 (line 535)
BB32
83   conditional branch(ne) v20,v22          (line 535)
BB33
85   goto                                    (line 535)
BB34
BB35
           v23 = phi  v16:#1,v9:#0
90   v24 = binaryop(add) v26 , v16:#1        (line 534)
BB36
           v32 = phi  v30,v32
           v25 = phi  v16:#1,v23
           v26 = phi  v16:#1,v24
94   conditional branch(ge) v26,v13          (line 534)
BB37
97   conditional branch(ne) v25,v9:#0        (line 534)
BB38
100   conditional branch(eq) v25,v9:#0       (line 536)
BB39
103   goto                                   (line 537)
BB40
106   v33 = binaryop(sub) v12 , v18          (line 538)
108   conditional branch(ge) v33,v13         (line 538)
BB41
110   return v5:#-1                          (line 539)
BB42
113   v34 = binaryop(add) v18 , v16:#1       (line 541)
BB43
           v27 = phi  v5:#-1,v18,v32
           v28 = phi  v9:#0,v25,v25
           v29 = phi  v2,v18,v34
117   conditional branch(eq) v28,v9:#0       (line 518)
BB44
119   return v27                             (line 543)
BB45

**CGNode:** Node: < Application, Lorg/apache/catalina/tribes/util/Arrays, toString([B)Ljava/lang/String; > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/membership/MemberImpl, <clinit>()V >:NEW <Primordial,[B>@15 in Everywhere} ]
**IR:** < Application, Lorg/apache/catalina/tribes/util/Arrays, toString([B)Ljava/lang/String; >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..4]
    -> BB4
    -> BB2
BB2[5..6]
    -> BB3
    -> BB7
BB3[7..7]
    -> BB5
BB4[8..8]
    -> BB5
BB5[9..9]
    -> BB6
    -> BB7
BB6[10..10]
    -> BB7
BB7[-1..-2]
Instructions:
BB0
BB1
4   conditional branch(eq) v1,v4:#null       (line 54)
BB2
6   v5 = arraylength v1                      (line 54)
BB3
7   goto                                     (line 54)
BB4
BB5
           v6 = phi  v5,v3:#0
9   v8 = invokestatic < Application, Lorg/apache/catalina/tribes/util/Arrays, toString([BII)Ljava/lang/String; > v1,v3:#0,v6 @12 exception:v7(line 54)
BB6
10   return v8                               (line 54)
BB7

**CGNode:** Node: < Application, Lorg/apache/catalina/tribes/util/Arrays, <clinit>()V > Context: Everywhere
**IR:** < Application, Lorg/apache/catalina/tribes/util/Arrays, <clinit>()V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..1]
    -> BB2
    -> BB3
BB2[2..3]
    -> BB3
BB3[-1..-2]
Instructions:
BB0
BB1
1   v4 = invokestatic < Application, Ljava/nio/charset/Charset, forName(Ljava/lang/String;)Ljava/nio/charset/Charset; > v2:#ISO-8859-1 @2 exception:v3(line 37)
BB2
2   putstatic v4 < Application, Lorg/apache/catalina/tribes/util/Arrays, CHARSET_ISO_8859_1, <Application,Ljava/nio/charset/Charset> >(line 36)
3   return                                   (line 35)
BB3

**CGNode:** Node: < Application, Lorg/apache/catalina/tribes/util/Arrays, toString([B)Ljava/lang/String; > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/membership/MemberImpl, <clinit>()V >:NEW <Primordial,[B>@69 in Everywhere} ]
**IR:** < Application, Lorg/apache/catalina/tribes/util/Arrays, toString([B)Ljava/lang/String; >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..4]
    -> BB4
    -> BB2
BB2[5..6]
    -> BB3
    -> BB7
BB3[7..7]
    -> BB5
BB4[8..8]
    -> BB5
BB5[9..9]
    -> BB6
    -> BB7
BB6[10..10]
    -> BB7
BB7[-1..-2]
Instructions:
BB0
BB1
4   conditional branch(eq) v1,v4:#null       (line 54)
BB2
6   v5 = arraylength v1                      (line 54)
BB3
7   goto                                     (line 54)
BB4
BB5
           v6 = phi  v5,v3:#0
9   v8 = invokestatic < Application, Lorg/apache/catalina/tribes/util/Arrays, toString([BII)Ljava/lang/String; > v1,v3:#0,v6 @12 exception:v7(line 54)
BB6
10   return v8                               (line 54)
BB7

**CGNode:** Node: < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, setHost([B)V > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/membership/MemberImpl, getMember([BII)Lorg/apache/catalina/tribes/membership/MemberImpl; >:NEW <Application,Lorg/apache/catalina/tribes/membership/MemberImpl>@3 in ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, main([Ljava/lang/String;)V >:NEW <Application,Lorg/apache/catalina/tribes/io/XByteBuffer>@19 in ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,[Ljava/lang/String>@1 in Everywhere} ]} ]} ]
**IR:** < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, setHost([B)V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..2]
    -> BB2
    -> BB3
BB2[3..3]
    -> BB3
BB3[-1..-2]
Instructions:
BB0
BB1
2   putfield v1 = v2 < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, host, <Primordial,[B> >(line 579)
BB2
3   return                                   (line 580)
BB3

**CGNode:** Node: < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, toInt([BI)I > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/membership/MemberImpl, getMember([BIILorg/apache/catalina/tribes/membership/MemberImpl;)Lorg/apache/catalina/tribes/membership/MemberImpl; >:NEW <Primordial,[B>@184 in ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, main([Ljava/lang/String;)V >:NEW <Application,Lorg/apache/catalina/tribes/io/XByteBuffer>@19 in ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,[Ljava/lang/String>@1 in Everywhere} ]} ]} ]
**IR:** < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, toInt([BI)I >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..4]
    -> BB2
    -> BB6
BB2[5..11]
    -> BB3
    -> BB6
BB3[12..21]
    -> BB4
    -> BB6
BB4[22..31]
    -> BB5
    -> BB6
BB5[32..37]
    -> BB6
BB6[-1..-2]
Instructions:
BB0
BB1
3   v5 = binaryop(add) v2 , v4:#3            (line 396)
4   v6 = arrayload v1[v5]                    (line 396)
BB2
6   v8 = binaryop(and) v6 , v7:#255          (line 396)
10   v10 = binaryop(add) v2 , v9:#2          (line 397)
11   v11 = arrayload v1[v10]                 (line 397)
BB3
13   v12 = binaryop(and) v11 , v7:#255       (line 397)
15   v14 = binaryop(SHL) v12 , v13:#8        (line 397)
16   v15 = binaryop(add) v8 , v14            (line 396)
20   v17 = binaryop(add) v2 , v16:#1         (line 398)
21   v18 = arrayload v1[v17]                 (line 398)
BB4
23   v19 = binaryop(and) v18 , v7:#255       (line 398)
25   v21 = binaryop(SHL) v19 , v20:#16       (line 398)
26   v22 = binaryop(add) v15 , v21           (line 396)
30   v24 = binaryop(add) v2 , v23:#0         (line 399)
31   v25 = arrayload v1[v24]                 (line 399)
BB5
33   v26 = binaryop(and) v25 , v7:#255       (line 399)
35   v28 = binaryop(SHL) v26 , v27:#24       (line 399)
36   v29 = binaryop(add) v22 , v28           (line 396)
37   return v29                              (line 396)
BB6

**CGNode:** Node: < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, setPort(I)V > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/membership/MemberImpl, getMember([BII)Lorg/apache/catalina/tribes/membership/MemberImpl; >:NEW <Application,Lorg/apache/catalina/tribes/membership/MemberImpl>@3 in ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, main([Ljava/lang/String;)V >:NEW <Application,Lorg/apache/catalina/tribes/io/XByteBuffer>@19 in ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,[Ljava/lang/String>@1 in Everywhere} ]} ]} ]
**IR:** < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, setPort(I)V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..2]
    -> BB2
    -> BB4
BB2[3..5]
    -> BB3
    -> BB4
BB3[6..6]
    -> BB4
BB4[-1..-2]
Instructions:
BB0
BB1
2   putfield v1 = v2 < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, port, <Primordial,I> >(line 592)
BB2
5   putfield v1 = v4:#null < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, dataPkg, <Primordial,[B> >(line 593)
BB3
6   return                                   (line 594)
BB4

**CGNode:** Node: < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, toInt([BI)I > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/membership/MemberImpl, getMember([BIILorg/apache/catalina/tribes/membership/MemberImpl;)Lorg/apache/catalina/tribes/membership/MemberImpl; >:NEW <Primordial,[B>@202 in ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, main([Ljava/lang/String;)V >:NEW <Application,Lorg/apache/catalina/tribes/io/XByteBuffer>@19 in ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,[Ljava/lang/String>@1 in Everywhere} ]} ]} ]
**IR:** < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, toInt([BI)I >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..4]
    -> BB2
    -> BB6
BB2[5..11]
    -> BB3
    -> BB6
BB3[12..21]
    -> BB4
    -> BB6
BB4[22..31]
    -> BB5
    -> BB6
BB5[32..37]
    -> BB6
BB6[-1..-2]
Instructions:
BB0
BB1
3   v5 = binaryop(add) v2 , v4:#3            (line 396)
4   v6 = arrayload v1[v5]                    (line 396)
BB2
6   v8 = binaryop(and) v6 , v7:#255          (line 396)
10   v10 = binaryop(add) v2 , v9:#2          (line 397)
11   v11 = arrayload v1[v10]                 (line 397)
BB3
13   v12 = binaryop(and) v11 , v7:#255       (line 397)
15   v14 = binaryop(SHL) v12 , v13:#8        (line 397)
16   v15 = binaryop(add) v8 , v14            (line 396)
20   v17 = binaryop(add) v2 , v16:#1         (line 398)
21   v18 = arrayload v1[v17]                 (line 398)
BB4
23   v19 = binaryop(and) v18 , v7:#255       (line 398)
25   v21 = binaryop(SHL) v19 , v20:#16       (line 398)
26   v22 = binaryop(add) v15 , v21           (line 396)
30   v24 = binaryop(add) v2 , v23:#0         (line 399)
31   v25 = arrayload v1[v24]                 (line 399)
BB5
33   v26 = binaryop(and) v25 , v7:#255       (line 399)
35   v28 = binaryop(SHL) v26 , v27:#24       (line 399)
36   v29 = binaryop(add) v22 , v28           (line 396)
37   return v29                              (line 396)
BB6

**CGNode:** Node: < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, setSecurePort(I)V > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/membership/MemberImpl, getMember([BII)Lorg/apache/catalina/tribes/membership/MemberImpl; >:NEW <Application,Lorg/apache/catalina/tribes/membership/MemberImpl>@3 in ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, main([Ljava/lang/String;)V >:NEW <Application,Lorg/apache/catalina/tribes/io/XByteBuffer>@19 in ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,[Ljava/lang/String>@1 in Everywhere} ]} ]} ]
**IR:** < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, setSecurePort(I)V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..2]
    -> BB2
    -> BB4
BB2[3..5]
    -> BB3
    -> BB4
BB3[6..6]
    -> BB4
BB4[-1..-2]
Instructions:
BB0
BB1
2   putfield v1 = v2 < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, securePort, <Primordial,I> >(line 626)
BB2
5   putfield v1 = v4:#null < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, dataPkg, <Primordial,[B> >(line 627)
BB3
6   return                                   (line 628)
BB4

**CGNode:** Node: < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, toInt([BI)I > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/membership/MemberImpl, getMember([BIILorg/apache/catalina/tribes/membership/MemberImpl;)Lorg/apache/catalina/tribes/membership/MemberImpl; >:NEW <Primordial,[B>@220 in ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, main([Ljava/lang/String;)V >:NEW <Application,Lorg/apache/catalina/tribes/io/XByteBuffer>@19 in ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,[Ljava/lang/String>@1 in Everywhere} ]} ]} ]
**IR:** < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, toInt([BI)I >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..4]
    -> BB2
    -> BB6
BB2[5..11]
    -> BB3
    -> BB6
BB3[12..21]
    -> BB4
    -> BB6
BB4[22..31]
    -> BB5
    -> BB6
BB5[32..37]
    -> BB6
BB6[-1..-2]
Instructions:
BB0
BB1
3   v5 = binaryop(add) v2 , v4:#3            (line 396)
4   v6 = arrayload v1[v5]                    (line 396)
BB2
6   v8 = binaryop(and) v6 , v7:#255          (line 396)
10   v10 = binaryop(add) v2 , v9:#2          (line 397)
11   v11 = arrayload v1[v10]                 (line 397)
BB3
13   v12 = binaryop(and) v11 , v7:#255       (line 397)
15   v14 = binaryop(SHL) v12 , v13:#8        (line 397)
16   v15 = binaryop(add) v8 , v14            (line 396)
20   v17 = binaryop(add) v2 , v16:#1         (line 398)
21   v18 = arrayload v1[v17]                 (line 398)
BB4
23   v19 = binaryop(and) v18 , v7:#255       (line 398)
25   v21 = binaryop(SHL) v19 , v20:#16       (line 398)
26   v22 = binaryop(add) v15 , v21           (line 396)
30   v24 = binaryop(add) v2 , v23:#0         (line 399)
31   v25 = arrayload v1[v24]                 (line 399)
BB5
33   v26 = binaryop(and) v25 , v7:#255       (line 399)
35   v28 = binaryop(SHL) v26 , v27:#24       (line 399)
36   v29 = binaryop(add) v22 , v28           (line 396)
37   return v29                              (line 396)
BB6

**CGNode:** Node: < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, setUdpPort(I)V > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/membership/MemberImpl, getMember([BII)Lorg/apache/catalina/tribes/membership/MemberImpl; >:NEW <Application,Lorg/apache/catalina/tribes/membership/MemberImpl>@3 in ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, main([Ljava/lang/String;)V >:NEW <Application,Lorg/apache/catalina/tribes/io/XByteBuffer>@19 in ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,[Ljava/lang/String>@1 in Everywhere} ]} ]} ]
**IR:** < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, setUdpPort(I)V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..2]
    -> BB2
    -> BB4
BB2[3..5]
    -> BB3
    -> BB4
BB3[6..6]
    -> BB4
BB4[-1..-2]
Instructions:
BB0
BB1
2   putfield v1 = v2 < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, udpPort, <Primordial,I> >(line 631)
BB2
5   putfield v1 = v4:#null < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, dataPkg, <Primordial,[B> >(line 632)
BB3
6   return                                   (line 633)
BB4

**CGNode:** Node: < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, toLong([BI)J > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/membership/MemberImpl, getMember([BIILorg/apache/catalina/tribes/membership/MemberImpl;)Lorg/apache/catalina/tribes/membership/MemberImpl; >:NEW <Primordial,[B>@165 in ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, main([Ljava/lang/String;)V >:NEW <Application,Lorg/apache/catalina/tribes/io/XByteBuffer>@19 in ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,[Ljava/lang/String>@1 in Everywhere} ]} ]} ]
**IR:** < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, toLong([BI)J >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..4]
    -> BB2
    -> BB10
BB2[5..12]
    -> BB3
    -> BB10
BB3[13..23]
    -> BB4
    -> BB10
BB4[24..34]
    -> BB5
    -> BB10
BB5[35..45]
    -> BB6
    -> BB10
BB6[46..56]
    -> BB7
    -> BB10
BB7[57..67]
    -> BB8
    -> BB10
BB8[68..78]
    -> BB9
    -> BB10
BB9[79..85]
    -> BB10
BB10[-1..-2]
Instructions:
BB0
BB1
3   v5 = binaryop(add) v2 , v4:#7            (line 410)
4   v6 = arrayload v1[v5]                    (line 410)
BB2
5   v7 = conversion(J) v6                    (line 410)
7   v9 = binaryop(and) v7 , v8:#255          (line 410)
11   v11 = binaryop(add) v2 , v10:#6         (line 411)
12   v12 = arrayload v1[v11]                 (line 411)
BB3
13   v13 = conversion(J) v12                 (line 411)
15   v14 = binaryop(and) v13 , v8:#255       (line 411)
17   v16 = binaryop(SHL) v14 , v15:#8        (line 411)
18   v17 = binaryop(add) v9 , v16            (line 410)
22   v19 = binaryop(add) v2 , v18:#5         (line 412)
23   v20 = arrayload v1[v19]                 (line 412)
BB4
24   v21 = conversion(J) v20                 (line 412)
26   v22 = binaryop(and) v21 , v8:#255       (line 412)
28   v24 = binaryop(SHL) v22 , v23:#16       (line 412)
29   v25 = binaryop(add) v17 , v24           (line 410)
33   v27 = binaryop(add) v2 , v26:#4         (line 413)
34   v28 = arrayload v1[v27]                 (line 413)
BB5
35   v29 = conversion(J) v28                 (line 413)
37   v30 = binaryop(and) v29 , v8:#255       (line 413)
39   v32 = binaryop(SHL) v30 , v31:#24       (line 413)
40   v33 = binaryop(add) v25 , v32           (line 410)
44   v35 = binaryop(add) v2 , v34:#3         (line 414)
45   v36 = arrayload v1[v35]                 (line 414)
BB6
46   v37 = conversion(J) v36                 (line 414)
48   v38 = binaryop(and) v37 , v8:#255       (line 414)
50   v40 = binaryop(SHL) v38 , v39:#32       (line 414)
51   v41 = binaryop(add) v33 , v40           (line 410)
55   v43 = binaryop(add) v2 , v42:#2         (line 415)
56   v44 = arrayload v1[v43]                 (line 415)
BB7
57   v45 = conversion(J) v44                 (line 415)
59   v46 = binaryop(and) v45 , v8:#255       (line 415)
61   v48 = binaryop(SHL) v46 , v47:#40       (line 415)
62   v49 = binaryop(add) v41 , v48           (line 410)
66   v51 = binaryop(add) v2 , v50:#1         (line 416)
67   v52 = arrayload v1[v51]                 (line 416)
BB8
68   v53 = conversion(J) v52                 (line 416)
70   v54 = binaryop(and) v53 , v8:#255       (line 416)
72   v56 = binaryop(SHL) v54 , v55:#48       (line 416)
73   v57 = binaryop(add) v49 , v56           (line 410)
77   v59 = binaryop(add) v2 , v58:#0         (line 417)
78   v60 = arrayload v1[v59]                 (line 417)
BB9
79   v61 = conversion(J) v60                 (line 417)
81   v62 = binaryop(and) v61 , v8:#255       (line 417)
83   v64 = binaryop(SHL) v62 , v63:#56       (line 417)
84   v65 = binaryop(add) v57 , v64           (line 410)
85   return v65                              (line 410)
BB10

**CGNode:** Node: < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, setMemberAliveTime(J)V > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/membership/MemberImpl, getMember([BII)Lorg/apache/catalina/tribes/membership/MemberImpl; >:NEW <Application,Lorg/apache/catalina/tribes/membership/MemberImpl>@3 in ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, main([Ljava/lang/String;)V >:NEW <Application,Lorg/apache/catalina/tribes/io/XByteBuffer>@19 in ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,[Ljava/lang/String>@1 in Everywhere} ]} ]} ]
**IR:** < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, setMemberAliveTime(J)V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..2]
    -> BB2
    -> BB3
BB2[3..3]
    -> BB3
BB3[-1..-2]
Instructions:
BB0
BB1
2   putfield v1 = v2 < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, memberAliveTime, <Primordial,J> >(line 513)
BB2
3   return                                   (line 514)
BB3

**CGNode:** Node: < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, setUniqueId([B)V > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/membership/MemberImpl, getMember([BII)Lorg/apache/catalina/tribes/membership/MemberImpl; >:NEW <Application,Lorg/apache/catalina/tribes/membership/MemberImpl>@3 in ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, main([Ljava/lang/String;)V >:NEW <Application,Lorg/apache/catalina/tribes/io/XByteBuffer>@19 in ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,[Ljava/lang/String>@1 in Everywhere} ]} ]} ]
**IR:** < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, setUniqueId([B)V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..3]
    -> BB3
    -> BB2
BB2[4..5]
    -> BB4
BB3[6..7]
    -> BB4
    -> BB7
BB4[8..8]
    -> BB5
    -> BB7
BB5[9..12]
    -> BB6
    -> BB7
BB6[13..14]
    -> BB7
BB7[-1..-2]
Instructions:
BB0
BB1
3   conditional branch(eq) v2,v4:#null       (line 601)
BB2
5   goto                                     (line 601)
BB3
7   v6 = new <Primordial,[B>@11v5:#16        (line 601)
BB4
           v7 = phi  v2,v6
8   putfield v1 = v7 < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, uniqueId, <Primordial,[B> >(line 601)
BB5
12   v10 = invokevirtual < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, getData(ZZ)[B > v1,v8:#1,v8:#1 @19 exception:v9(line 602)
BB6
14   return                                  (line 603)
BB7

**CGNode:** Node: < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint$Acceptor$AcceptorState, <clinit>()V > Context: Everywhere
**IR:** < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint$Acceptor$AcceptorState, <clinit>()V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..0]
    -> BB2
    -> BB15
BB2[1..4]
    -> BB3
    -> BB15
BB3[5..6]
    -> BB4
    -> BB15
BB4[7..10]
    -> BB5
    -> BB15
BB5[11..12]
    -> BB6
    -> BB15
BB6[13..16]
    -> BB7
    -> BB15
BB7[17..18]
    -> BB8
    -> BB15
BB8[19..22]
    -> BB9
    -> BB15
BB9[23..25]
    -> BB10
    -> BB15
BB10[26..29]
    -> BB11
    -> BB15
BB11[30..33]
    -> BB12
    -> BB15
BB12[34..37]
    -> BB13
    -> BB15
BB13[38..41]
    -> BB14
    -> BB15
BB14[42..43]
    -> BB15
BB15[-1..-2]
Instructions:
BB0
BB1
0   v2 = new <Application,Lorg/apache/tomcat/util/net/AbstractEndpoint$Acceptor$AcceptorState>@0(line 82)
BB2
4   invokespecial < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint$Acceptor$AcceptorState, <init>(Ljava/lang/String;I)V > v2,v3:#NEW,v4:#0 @7 exception:v5(line 82)
BB3
5   putstatic v2 < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint$Acceptor$AcceptorState, NEW, <Application,Lorg/apache/tomcat/util/net/AbstractEndpoint$Acceptor$AcceptorState> >(line 82)
6   v6 = new <Application,Lorg/apache/tomcat/util/net/AbstractEndpoint$Acceptor$AcceptorState>@13(line 82)
BB4
10   invokespecial < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint$Acceptor$AcceptorState, <init>(Ljava/lang/String;I)V > v6,v7:#RUNNING,v8:#1 @20 exception:v9(line 82)
BB5
11   putstatic v6 < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint$Acceptor$AcceptorState, RUNNING, <Application,Lorg/apache/tomcat/util/net/AbstractEndpoint$Acceptor$AcceptorState> >(line 82)
12   v10 = new <Application,Lorg/apache/tomcat/util/net/AbstractEndpoint$Acceptor$AcceptorState>@26(line 82)
BB6
16   invokespecial < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint$Acceptor$AcceptorState, <init>(Ljava/lang/String;I)V > v10,v11:#PAUSED,v12:#2 @33 exception:v13(line 82)
BB7
17   putstatic v10 < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint$Acceptor$AcceptorState, PAUSED, <Application,Lorg/apache/tomcat/util/net/AbstractEndpoint$Acceptor$AcceptorState> >(line 82)
18   v14 = new <Application,Lorg/apache/tomcat/util/net/AbstractEndpoint$Acceptor$AcceptorState>@39(line 82)
BB8
22   invokespecial < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint$Acceptor$AcceptorState, <init>(Ljava/lang/String;I)V > v14,v15:#ENDED,v16:#3 @46 exception:v17(line 82)
BB9
23   putstatic v14 < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint$Acceptor$AcceptorState, ENDED, <Application,Lorg/apache/tomcat/util/net/AbstractEndpoint$Acceptor$AcceptorState> >(line 82)
25   v19 = new <Application,[Lorg/apache/tomcat/util/net/AbstractEndpoint$Acceptor$AcceptorState>@53v18:#4 (line 81)
BB10
28   v20 = getstatic < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint$Acceptor$AcceptorState, NEW, <Application,Lorg/apache/tomcat/util/net/AbstractEndpoint$Acceptor$AcceptorState> >(line 81)
29   arraystore v19[v4:#0] = v20             (line 81)
BB11
32   v21 = getstatic < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint$Acceptor$AcceptorState, RUNNING, <Application,Lorg/apache/tomcat/util/net/AbstractEndpoint$Acceptor$AcceptorState> >(line 81)
33   arraystore v19[v8:#1] = v21             (line 81)
BB12
36   v22 = getstatic < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint$Acceptor$AcceptorState, PAUSED, <Application,Lorg/apache/tomcat/util/net/AbstractEndpoint$Acceptor$AcceptorState> >(line 81)
37   arraystore v19[v12:#2] = v22            (line 81)
BB13
40   v23 = getstatic < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint$Acceptor$AcceptorState, ENDED, <Application,Lorg/apache/tomcat/util/net/AbstractEndpoint$Acceptor$AcceptorState> >(line 81)
41   arraystore v19[v16:#3] = v23            (line 81)
BB14
42   putstatic v19 < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint$Acceptor$AcceptorState, ENUM$VALUES, <Application,[Lorg/apache/tomcat/util/net/AbstractEndpoint$Acceptor$AcceptorState> >(line 81)
43   return                                  (line 81)
BB15

**CGNode:** Node: < Application, Lorg/apache/catalina/tribes/util/UUIDGenerator, nextBytes([BIILjava/util/Random;)V > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/io/ChannelData, generateUUID()V >:NEW <Primordial,[B>@2 in ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/io/ChannelData, getDataFromPackage(Lorg/apache/catalina/tribes/io/XByteBuffer;)Lorg/apache/catalina/tribes/io/ChannelData; >:NEW <Application,Lorg/apache/catalina/tribes/io/ChannelData>@0 in ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, main([Ljava/lang/String;)V >:NEW <Application,Lorg/apache/catalina/tribes/io/XByteBuffer>@19 in ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,[Ljava/lang/String>@1 in Everywhere} ]} ]} ]} ]
**IR:** < Application, Lorg/apache/catalina/tribes/util/UUIDGenerator, nextBytes([BIILjava/util/Random;)V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..5]
    -> BB2
BB2[6..8]
    -> BB11
BB3[9..11]
    -> BB5
    -> BB4
BB4[12..12]
    -> BB13
BB5[13..15]
    -> BB8
    -> BB6
BB6[16..17]
    -> BB7
    -> BB13
BB7[18..18]
    -> BB9
BB8[19..21]
    -> BB9
BB9[22..29]
    -> BB10
    -> BB13
BB10[30..37]
    -> BB11
BB11[38..40]
    -> BB3
    -> BB12
BB12[41..41]
    -> BB2
BB13[-1..-2]
Instructions:
BB0
BB1
BB2
           v21 = phi  v18,v6:#0
           v22 = phi  v19,v6:#0
8   goto                                     (line 83)
BB3
11   conditional branch(ne) v18,v3           (line 84)
BB4
12   return                                  (line 84)
BB5
15   conditional branch(ne) v20,v6:#0        (line 85)
BB6
17   v9 = invokevirtual < Application, Ljava/util/Random, nextInt()I > v4 @29 exception:v8(line 85)
BB7
18   goto                                    (line 85)
BB8
21   v11 = binaryop(SHR) v19 , v10:#8        (line 85)
BB9
           v12 = phi  v9,v11
26   v13 = binaryop(add) v2 , v18            (line 86)
28   v14 = conversion(B) v12                 (line 86)
29   arraystore v1[v13] = v14                (line 86)
BB10
32   v16 = binaryop(add) v18 , v15:#1        (line 87)
36   v17 = binaryop(add) v20 , v15:#1        (line 83)
BB11
           v18 = phi  v21,v16
           v19 = phi  v22,v12
           v20 = phi  v6:#0,v17
40   conditional branch(lt) v20,v7:#4        (line 83)
BB12
41   goto                                    (line 82)
BB13

**CGNode:** Node: < Application, Lorg/apache/catalina/tribes/util/StringManager, getManager(Ljava/lang/String;)Lorg/apache/catalina/tribes/util/StringManager; > Context: ReceiverStringContext: [ [<Primordial,Ljava/lang/String>] ]
**IR:** < Application, Lorg/apache/catalina/tribes/util/StringManager, getManager(Ljava/lang/String;)Lorg/apache/catalina/tribes/util/StringManager; >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..2]
    -> BB2
    -> BB9
BB2[3..3]
    -> BB3
    -> BB9
BB3[4..7]
    -> BB8
    -> BB4
BB4[8..8]
    -> BB5
    -> BB9
BB5[9..11]
    -> BB6
    -> BB9
BB6[12..16]
    -> BB7
    -> BB9
BB7[17..17]
    -> BB8
BB8[18..19]
    -> BB9
BB9[-1..-2]
Instructions:
BB0
BB1
0   v3 = getstatic < Application, Lorg/apache/catalina/tribes/util/StringManager, managers, <Application,Ljava/util/Hashtable> >(line 163)
2   v5 = invokevirtual < Application, Ljava/util/Hashtable, get(Ljava/lang/Object;)Ljava/lang/Object; > v3,v1 @4 exception:v4(line 163)
BB2
3   v6 = checkcast <Application,Lorg/apache/catalina/tribes/util/StringManager>v5(line 163)
BB3
7   conditional branch(ne) v6,v7:#null       (line 164)
BB4
8   v8 = new <Application,Lorg/apache/catalina/tribes/util/StringManager>@15(line 165)
BB5
11   invokespecial < Application, Lorg/apache/catalina/tribes/util/StringManager, <init>(Ljava/lang/String;)V > v8,v1 @20 exception:v9(line 165)
BB6
13   v10 = getstatic < Application, Lorg/apache/catalina/tribes/util/StringManager, managers, <Application,Ljava/util/Hashtable> >(line 166)
16   v12 = invokevirtual < Application, Ljava/util/Hashtable, put(Ljava/lang/Object;Ljava/lang/Object;)Ljava/lang/Object; > v10,v1,v8 @29 exception:v11(line 166)
BB7
BB8
           v13 = phi  v6,v8
19   return v13                              (line 168)
BB9

**CGNode:** Node: < Application, Lorg/apache/catalina/tribes/util/StringManager, <clinit>()V > Context: Everywhere
**IR:** < Application, Lorg/apache/catalina/tribes/util/StringManager, <clinit>()V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..0]
    -> BB2
    -> BB4
BB2[1..2]
    -> BB3
    -> BB4
BB3[3..4]
    -> BB4
BB4[-1..-2]
Instructions:
BB0
BB1
0   v2 = new <Application,Ljava/util/Hashtable>@0(line 153)
BB2
2   invokespecial < Application, Ljava/util/Hashtable, <init>()V > v2 @4 exception:v3(line 153)
BB3
3   putstatic v2 < Application, Lorg/apache/catalina/tribes/util/StringManager, managers, <Application,Ljava/util/Hashtable> >(line 152)
4   return                                   (line 53)
BB4

**CGNode:** Node: < Application, Lorg/apache/catalina/tribes/util/Arrays, toString([BII)Ljava/lang/String; > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/membership/MemberImpl, <clinit>()V >:NEW <Primordial,[B>@15 in Everywhere} ]
**IR:** < Application, Lorg/apache/catalina/tribes/util/Arrays, toString([BII)Ljava/lang/String; >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..4]
    -> BB2
    -> BB3
BB2[5..5]
    -> BB3
BB3[-1..-2]
Instructions:
BB0
BB1
4   v7 = invokestatic < Application, Lorg/apache/catalina/tribes/util/Arrays, toString([BIIZ)Ljava/lang/String; > v1,v2,v3,v5:#0 @4 exception:v6(line 58)
BB2
5   return v7                                (line 58)
BB3

**CGNode:** Node: < Application, Lorg/apache/catalina/tribes/util/Arrays, toString([BII)Ljava/lang/String; > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/membership/MemberImpl, <clinit>()V >:NEW <Primordial,[B>@69 in Everywhere} ]
**IR:** < Application, Lorg/apache/catalina/tribes/util/Arrays, toString([BII)Ljava/lang/String; >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..4]
    -> BB2
    -> BB3
BB2[5..5]
    -> BB3
BB3[-1..-2]
Instructions:
BB0
BB1
4   v7 = invokestatic < Application, Lorg/apache/catalina/tribes/util/Arrays, toString([BIIZ)Ljava/lang/String; > v1,v2,v3,v5:#0 @4 exception:v6(line 58)
BB2
5   return v7                                (line 58)
BB3

**CGNode:** Node: < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, getData(ZZ)[B > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/membership/MemberImpl, getMember([BII)Lorg/apache/catalina/tribes/membership/MemberImpl; >:NEW <Application,Lorg/apache/catalina/tribes/membership/MemberImpl>@3 in ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, main([Ljava/lang/String;)V >:NEW <Application,Lorg/apache/catalina/tribes/io/XByteBuffer>@19 in ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,[Ljava/lang/String>@1 in Everywhere} ]} ]} ]
**IR:** < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, getData(ZZ)[B >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..2]
    -> BB3
    -> BB2
BB2[3..5]
    -> BB3
    -> BB76
BB3[6..7]
    -> BB4
    -> BB76
BB4[8..9]
    -> BB14
    -> BB5
BB5[10..12]
    -> BB12
    -> BB6
BB6[13..13]
    -> BB7
    -> BB76
BB7[14..15]
    -> BB8
    -> BB76
BB8[16..20]
    -> BB9
    -> BB76
BB9[21..22]
    -> BB10
    -> BB76
BB10[23..25]
    -> BB11
    -> BB76
BB11[26..26]
    -> BB12
BB12[27..28]
    -> BB13
    -> BB76
BB13[29..29]
    -> BB76
BB14[30..31]
    -> BB15
    -> BB76
BB15[32..33]
    -> BB16
    -> BB76
BB16[34..35]
    -> BB17
    -> BB76
BB17[36..39]
    -> BB18
    -> BB76
BB18[40..43]
    -> BB19
    -> BB76
BB19[44..44]
    -> BB20
    -> BB76
BB20[45..47]
    -> BB21
    -> BB76
BB21[48..49]
    -> BB22
    -> BB76
BB22[50..52]
    -> BB23
    -> BB76
BB23[53..64]
    -> BB24
    -> BB76
BB24[65..65]
    -> BB25
    -> BB76
BB25[66..68]
    -> BB26
    -> BB76
BB26[69..74]
    -> BB27
    -> BB76
BB27[75..83]
    -> BB28
    -> BB76
BB28[84..90]
    -> BB29
    -> BB76
BB29[91..93]
    -> BB30
    -> BB76
BB30[94..100]
    -> BB31
    -> BB76
BB31[101..103]
    -> BB32
    -> BB76
BB32[104..110]
    -> BB33
    -> BB76
BB33[111..113]
    -> BB34
    -> BB76
BB34[114..126]
    -> BB35
    -> BB76
BB35[127..132]
    -> BB36
    -> BB76
BB36[133..133]
    -> BB37
    -> BB76
BB37[134..136]
    -> BB38
    -> BB76
BB38[137..140]
    -> BB39
    -> BB76
BB39[141..141]
    -> BB40
    -> BB76
BB40[142..144]
    -> BB41
    -> BB76
BB41[145..151]
    -> BB42
    -> BB76
BB42[152..156]
    -> BB43
    -> BB76
BB43[157..157]
    -> BB44
    -> BB76
BB44[158..158]
    -> BB45
    -> BB76
BB45[159..161]
    -> BB46
    -> BB76
BB46[162..162]
    -> BB47
    -> BB76
BB47[163..166]
    -> BB48
    -> BB76
BB48[167..167]
    -> BB49
    -> BB76
BB49[168..170]
    -> BB50
    -> BB76
BB50[171..177]
    -> BB51
    -> BB76
BB51[178..182]
    -> BB52
    -> BB76
BB52[183..183]
    -> BB53
    -> BB76
BB53[184..184]
    -> BB54
    -> BB76
BB54[185..187]
    -> BB55
    -> BB76
BB55[188..188]
    -> BB56
    -> BB76
BB56[189..192]
    -> BB57
    -> BB76
BB57[193..197]
    -> BB58
    -> BB76
BB58[198..198]
    -> BB59
    -> BB76
BB59[199..199]
    -> BB60
    -> BB76
BB60[200..202]
    -> BB61
    -> BB76
BB61[203..203]
    -> BB62
    -> BB76
BB62[204..207]
    -> BB63
    -> BB76
BB63[208..208]
    -> BB64
    -> BB76
BB64[209..211]
    -> BB65
    -> BB76
BB65[212..218]
    -> BB66
    -> BB76
BB66[219..223]
    -> BB67
    -> BB76
BB67[224..224]
    -> BB68
    -> BB76
BB68[225..225]
    -> BB69
    -> BB76
BB69[226..228]
    -> BB70
    -> BB76
BB70[229..229]
    -> BB71
    -> BB76
BB71[230..237]
    -> BB72
    -> BB76
BB72[238..238]
    -> BB73
    -> BB76
BB73[239..241]
    -> BB74
    -> BB76
BB74[242..246]
    -> BB75
    -> BB76
BB75[247..248]
    -> BB76
BB76[-1..-2]
Instructions:
BB0
BB1
2   conditional branch(eq) v3,v5:#0          (line 210)
BB2
5   putfield v1 = v6:#null < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, dataPkg, <Primordial,[B> >(line 210)
BB3
7   v7 = getfield < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, dataPkg, <Primordial,[B> > v1(line 212)
BB4
9   conditional branch(eq) v7,v6:#null       (line 212)
BB5
12   conditional branch(eq) v2,v5:#0         (line 213)
BB6
13   v112 = invokestatic < Application, Ljava/lang/System, currentTimeMillis()J > @20 exception:v111(line 216)
BB7
15   v114 = invokevirtual < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, getServiceStartTime()J > v1 @24 exception:v113(line 216)
BB8
16   v115 = binaryop(sub) v112 , v114        (line 216)
20   v116 = getfield < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, dataPkg, <Primordial,[B> > v1(line 217)
BB9
21   v117 = getstatic < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, TRIBES_MBR_BEGIN, <Primordial,[B> >(line 217)
22   v118 = arraylength v117                 (line 217)
BB10
24   v119 = binaryop(add) v118 , v27:#4      (line 217)
25   v121 = invokestatic < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, toBytes(J[BI)[B > v115,v116,v119 @40 exception:v120(line 217)
BB11
BB12
28   v122 = getfield < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, dataPkg, <Primordial,[B> > v1(line 219)
BB13
29   return v122                             (line 219)
BB14
31   v8 = getfield < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, host, <Primordial,[B> > v1(line 239)
BB15
33   v10 = invokestatic < Application, Ljava/lang/System, currentTimeMillis()J > @54 exception:v9(line 240)
BB16
35   v12 = invokevirtual < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, getServiceStartTime()J > v1 @58 exception:v11(line 240)
BB17
36   v13 = binaryop(sub) v10 , v12           (line 240)
39   v14 = arraylength v8                    (line 241)
BB18
40   v15 = conversion(B) v14                 (line 241)
43   v17 = invokevirtual < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, getDataLength()I > v1 @70 exception:v16(line 242)
BB19
44   v18 = new <Primordial,[B>@73v17         (line 242)
BB20
47   v20 = invokevirtual < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, getDataLength()I > v1 @78 exception:v19(line 244)
BB21
48   v21 = getstatic < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, TRIBES_MBR_BEGIN, <Primordial,[B> >(line 244)
49   v22 = arraylength v21                   (line 244)
BB22
50   v23 = binaryop(sub) v20 , v22           (line 244)
51   v24 = getstatic < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, TRIBES_MBR_END, <Primordial,[B> >(line 244)
52   v25 = arraylength v24                   (line 244)
BB23
53   v26 = binaryop(sub) v23 , v25           (line 244)
55   v28 = binaryop(sub) v26 , v27:#4        (line 244)
59   v29 = getstatic < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, TRIBES_MBR_BEGIN, <Primordial,[B> >(line 249)
63   v30 = getstatic < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, TRIBES_MBR_BEGIN, <Primordial,[B> >(line 249)
64   v31 = arraylength v30                   (line 249)
BB24
65   invokestatic < Application, Ljava/lang/System, arraycopy(Ljava/lang/Object;ILjava/lang/Object;II)V > v29,v5:#0,v18,v5:#0,v31 @110 exception:v32(line 249)
BB25
67   v33 = getstatic < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, TRIBES_MBR_BEGIN, <Primordial,[B> >(line 250)
68   v34 = arraylength v33                   (line 250)
BB26
69   v35 = binaryop(add) v5:#0 , v34         (line 250)
74   v37 = invokestatic < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, toBytes(I[BI)[B > v28,v18,v35 @128 exception:v36(line 253)
BB27
78   v38 = binaryop(add) v35 , v27:#4        (line 254)
83   v40 = invokestatic < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, toBytes(J[BI)[B > v13,v18,v38 @141 exception:v39(line 257)
BB28
87   v42 = binaryop(add) v38 , v41:#8        (line 258)
90   v43 = getfield < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, port, <Primordial,I> > v1(line 260)
BB29
93   v45 = invokestatic < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, toBytes(I[BI)[B > v43,v18,v42 @156 exception:v44(line 260)
BB30
97   v46 = binaryop(add) v42 , v27:#4        (line 261)
100   v47 = getfield < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, securePort, <Primordial,I> > v1(line 263)
BB31
103   v49 = invokestatic < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, toBytes(I[BI)[B > v47,v18,v46 @171 exception:v48(line 263)
BB32
107   v50 = binaryop(add) v46 , v27:#4       (line 264)
110   v51 = getfield < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, udpPort, <Primordial,I> > v1(line 266)
BB33
113   v53 = invokestatic < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, toBytes(I[BI)[B > v51,v18,v50 @186 exception:v52(line 266)
BB34
117   v54 = binaryop(add) v50 , v27:#4       (line 267)
123   v56 = binaryop(add) v54 , v55:#1       (line 269)
126   arraystore v18[v54] = v15              (line 269)
BB35
132   v57 = arraylength v8                   (line 271)
BB36
133   invokestatic < Application, Ljava/lang/System, arraycopy(Ljava/lang/Object;ILjava/lang/Object;II)V > v8,v5:#0,v18,v56,v57 @211 exception:v58(line 271)
BB37
136   v59 = arraylength v8                   (line 272)
BB38
137   v60 = binaryop(add) v56 , v59          (line 272)
140   v61 = getfield < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, command, <Primordial,[B> > v1(line 274)
BB39
141   v62 = arraylength v61                  (line 274)
BB40
144   v64 = invokestatic < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, toBytes(I[BI)[B > v62,v18,v60 @230 exception:v63(line 274)
BB41
148   v65 = binaryop(add) v60 , v27:#4       (line 275)
151   v66 = getfield < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, command, <Primordial,[B> > v1(line 277)
BB42
156   v67 = getfield < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, command, <Primordial,[B> > v1(line 277)
BB43
157   v68 = arraylength v67                  (line 277)
BB44
158   invokestatic < Application, Ljava/lang/System, arraycopy(Ljava/lang/Object;ILjava/lang/Object;II)V > v66,v5:#0,v18,v65,v68 @251 exception:v69(line 277)
BB45
161   v70 = getfield < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, command, <Primordial,[B> > v1(line 278)
BB46
162   v71 = arraylength v70                  (line 278)
BB47
163   v72 = binaryop(add) v65 , v71          (line 278)
166   v73 = getfield < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, domain, <Primordial,[B> > v1(line 280)
BB48
167   v74 = arraylength v73                  (line 280)
BB49
170   v76 = invokestatic < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, toBytes(I[BI)[B > v74,v18,v72 @273 exception:v75(line 280)
BB50
174   v77 = binaryop(add) v72 , v27:#4       (line 281)
177   v78 = getfield < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, domain, <Primordial,[B> > v1(line 283)
BB51
182   v79 = getfield < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, domain, <Primordial,[B> > v1(line 283)
BB52
183   v80 = arraylength v79                  (line 283)
BB53
184   invokestatic < Application, Ljava/lang/System, arraycopy(Ljava/lang/Object;ILjava/lang/Object;II)V > v78,v5:#0,v18,v77,v80 @294 exception:v81(line 283)
BB54
187   v82 = getfield < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, domain, <Primordial,[B> > v1(line 284)
BB55
188   v83 = arraylength v82                  (line 284)
BB56
189   v84 = binaryop(add) v77 , v83          (line 284)
192   v85 = getfield < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, uniqueId, <Primordial,[B> > v1(line 286)
BB57
197   v86 = getfield < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, uniqueId, <Primordial,[B> > v1(line 286)
BB58
198   v87 = arraylength v86                  (line 286)
BB59
199   invokestatic < Application, Ljava/lang/System, arraycopy(Ljava/lang/Object;ILjava/lang/Object;II)V > v85,v5:#0,v18,v84,v87 @321 exception:v88(line 286)
BB60
202   v89 = getfield < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, uniqueId, <Primordial,[B> > v1(line 287)
BB61
203   v90 = arraylength v89                  (line 287)
BB62
204   v91 = binaryop(add) v84 , v90          (line 287)
207   v92 = getfield < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, payload, <Primordial,[B> > v1(line 289)
BB63
208   v93 = arraylength v92                  (line 289)
BB64
211   v95 = invokestatic < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, toBytes(I[BI)[B > v93,v18,v91 @343 exception:v94(line 289)
BB65
215   v96 = binaryop(add) v91 , v27:#4       (line 290)
218   v97 = getfield < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, payload, <Primordial,[B> > v1(line 291)
BB66
223   v98 = getfield < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, payload, <Primordial,[B> > v1(line 291)
BB67
224   v99 = arraylength v98                  (line 291)
BB68
225   invokestatic < Application, Ljava/lang/System, arraycopy(Ljava/lang/Object;ILjava/lang/Object;II)V > v97,v5:#0,v18,v96,v99 @364 exception:v100(line 291)
BB69
228   v101 = getfield < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, payload, <Primordial,[B> > v1(line 292)
BB70
229   v102 = arraylength v101                (line 292)
BB71
230   v103 = binaryop(add) v96 , v102        (line 292)
232   v104 = getstatic < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, TRIBES_MBR_END, <Primordial,[B> >(line 295)
236   v105 = getstatic < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, TRIBES_MBR_END, <Primordial,[B> >(line 295)
237   v106 = arraylength v105                (line 295)
BB72
238   invokestatic < Application, Ljava/lang/System, arraycopy(Ljava/lang/Object;ILjava/lang/Object;II)V > v104,v5:#0,v18,v103,v106 @389 exception:v107(line 295)
BB73
240   v108 = getstatic < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, TRIBES_MBR_END, <Primordial,[B> >(line 296)
241   v109 = arraylength v108                (line 296)
BB74
242   v110 = binaryop(add) v103 , v109       (line 296)
246   putfield v1 = v18 < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, dataPkg, <Primordial,[B> >(line 299)
BB75
248   return v18                             (line 300)
BB76

**CGNode:** Node: < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint$Acceptor$AcceptorState, <init>(Ljava/lang/String;I)V > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/tomcat/util/net/AbstractEndpoint$Acceptor$AcceptorState, <clinit>()V >:NEW <Application,Lorg/apache/tomcat/util/net/AbstractEndpoint$Acceptor$AcceptorState>@0 in Everywhere} ]
**IR:** < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint$Acceptor$AcceptorState, <init>(Ljava/lang/String;I)V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..3]
    -> BB2
    -> BB3
BB2[4..4]
    -> BB3
BB3[-1..-2]
Instructions:
BB0
BB1
3   invokespecial < Application, Ljava/lang/Enum, <init>(Ljava/lang/String;I)V > v1,v2,v3 @3 exception:v5(line 81)
BB2
4   return                                   (line 81)
BB3

**CGNode:** Node: < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint$Acceptor$AcceptorState, <init>(Ljava/lang/String;I)V > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/tomcat/util/net/AbstractEndpoint$Acceptor$AcceptorState, <clinit>()V >:NEW <Application,Lorg/apache/tomcat/util/net/AbstractEndpoint$Acceptor$AcceptorState>@13 in Everywhere} ]
**IR:** < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint$Acceptor$AcceptorState, <init>(Ljava/lang/String;I)V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..3]
    -> BB2
    -> BB3
BB2[4..4]
    -> BB3
BB3[-1..-2]
Instructions:
BB0
BB1
3   invokespecial < Application, Ljava/lang/Enum, <init>(Ljava/lang/String;I)V > v1,v2,v3 @3 exception:v5(line 81)
BB2
4   return                                   (line 81)
BB3

**CGNode:** Node: < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint$Acceptor$AcceptorState, <init>(Ljava/lang/String;I)V > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/tomcat/util/net/AbstractEndpoint$Acceptor$AcceptorState, <clinit>()V >:NEW <Application,Lorg/apache/tomcat/util/net/AbstractEndpoint$Acceptor$AcceptorState>@26 in Everywhere} ]
**IR:** < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint$Acceptor$AcceptorState, <init>(Ljava/lang/String;I)V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..3]
    -> BB2
    -> BB3
BB2[4..4]
    -> BB3
BB3[-1..-2]
Instructions:
BB0
BB1
3   invokespecial < Application, Ljava/lang/Enum, <init>(Ljava/lang/String;I)V > v1,v2,v3 @3 exception:v5(line 81)
BB2
4   return                                   (line 81)
BB3

**CGNode:** Node: < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint$Acceptor$AcceptorState, <init>(Ljava/lang/String;I)V > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/tomcat/util/net/AbstractEndpoint$Acceptor$AcceptorState, <clinit>()V >:NEW <Application,Lorg/apache/tomcat/util/net/AbstractEndpoint$Acceptor$AcceptorState>@39 in Everywhere} ]
**IR:** < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint$Acceptor$AcceptorState, <init>(Ljava/lang/String;I)V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..3]
    -> BB2
    -> BB3
BB2[4..4]
    -> BB3
BB3[-1..-2]
Instructions:
BB0
BB1
3   invokespecial < Application, Ljava/lang/Enum, <init>(Ljava/lang/String;I)V > v1,v2,v3 @3 exception:v5(line 81)
BB2
4   return                                   (line 81)
BB3

**CGNode:** Node: < Application, Lorg/apache/catalina/tribes/util/StringManager, <init>(Ljava/lang/String;)V > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/util/StringManager, getManager(Ljava/lang/String;)Lorg/apache/catalina/tribes/util/StringManager; >:NEW <Application,Lorg/apache/catalina/tribes/util/StringManager>@15 in ReceiverStringContext: [ [<Primordial,Ljava/lang/String>] ]} ]
**IR:** < Application, Lorg/apache/catalina/tribes/util/StringManager, <init>(Ljava/lang/String;)V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..1]
    -> BB2
    -> BB25
BB2[2..2]
    -> BB3
    -> BB25
BB3[3..5]
    -> BB4
    -> BB25
BB4[6..6]
    -> BB5
    -> BB25
BB5[7..8]
    -> BB6
    -> BB25
BB6[9..9]
    -> BB7
    -> BB25
BB7[10..13]
    -> BB8
    -> BB11
    -> BB25
BB8[14..14]
    -> BB9
    -> BB11
    -> BB25
BB9[15..15]
    -> BB10
    -> BB25
BB10[16..16]
    -> BB19
BB11[17..18]
    -> BB12
    -> BB25
BB12[19..19]
    -> BB13
    -> BB25
BB13[20..23]
    -> BB19
    -> BB14
BB14[24..26]
    -> BB15
    -> BB18
    -> BB25
BB15[27..28]
    -> BB16
    -> BB18
    -> BB25
BB16[29..29]
    -> BB17
    -> BB25
BB17[30..30]
    -> BB19
BB18[31..31]
    -> BB19
BB19[32..33]
    -> BB20
    -> BB25
BB20[34..35]
    -> BB24
    -> BB21
BB21[36..38]
    -> BB22
    -> BB25
BB22[39..39]
    -> BB23
    -> BB25
BB23[40..40]
    -> BB24
    -> BB25
BB24[41..41]
    -> BB25
BB25[-1..-2]
Instructions:
BB0
BB1
1   invokespecial < Application, Ljava/lang/Object, <init>()V > v1 @1 exception:v4(line 69)
BB2
2   v5 = new <Application,Ljava/lang/StringBuilder>@4(line 70)
BB3
5   v7 = invokestatic < Application, Ljava/lang/String, valueOf(Ljava/lang/Object;)Ljava/lang/String; > v2 @9 exception:v6(line 70)
BB4
6   invokespecial < Application, Ljava/lang/StringBuilder, <init>(Ljava/lang/String;)V > v5,v7 @12 exception:v8(line 70)
BB5
8   v11 = invokevirtual < Application, Ljava/lang/StringBuilder, append(Ljava/lang/String;)Ljava/lang/StringBuilder; > v5,v9:#.LocalStrings @17 exception:v10(line 70)
BB6
9   v13 = invokevirtual < Application, Ljava/lang/StringBuilder, toString()Ljava/lang/String; > v11 @20 exception:v12(line 70)
BB7
13   v15 = invokestatic < Application, Ljava/util/Locale, getDefault()Ljava/util/Locale; > @26 exception:v14(line 72)
BB8
14   v17 = invokestatic < Application, Ljava/util/ResourceBundle, getBundle(Ljava/lang/String;Ljava/util/Locale;)Ljava/util/ResourceBundle; > v13,v15 @29 exception:v16(line 72)
BB9
15   putfield v1 = v17 < Application, Lorg/apache/catalina/tribes/util/StringManager, bundle, <Application,Ljava/util/ResourceBundle> >(line 72)
BB10
16   goto                                    (line 72)
BB11<Handler>
           v18 = getCaughtException 
18   v20 = invokestatic < Application, Ljava/lang/Thread, currentThread()Ljava/lang/Thread; > @39 exception:v19(line 77)
BB12
19   v22 = invokevirtual < Application, Ljava/lang/Thread, getContextClassLoader()Ljava/lang/ClassLoader; > v20 @42 exception:v21(line 77)
BB13
23   conditional branch(eq) v22,v23:#null    (line 78)
BB14
26   v25 = invokestatic < Application, Ljava/util/Locale, getDefault()Ljava/util/Locale; > @54 exception:v24(line 81)
BB15
28   v27 = invokestatic < Application, Ljava/util/ResourceBundle, getBundle(Ljava/lang/String;Ljava/util/Locale;Ljava/lang/ClassLoader;)Ljava/util/ResourceBundle; > v13,v25,v22 @59 exception:v26(line 80)
BB16
29   putfield v1 = v27 < Application, Lorg/apache/catalina/tribes/util/StringManager, bundle, <Application,Ljava/util/ResourceBundle> >(line 80)
BB17
30   goto                                    (line 80)
BB18<Handler>
           v28 = getCaughtException 
BB19
33   v30 = getfield < Application, Lorg/apache/catalina/tribes/util/StringManager, bundle, <Application,Ljava/util/ResourceBundle> > v1(line 88)
BB20
35   conditional branch(eq) v30,v23:#null    (line 88)
BB21
38   v31 = getfield < Application, Lorg/apache/catalina/tribes/util/StringManager, bundle, <Application,Ljava/util/ResourceBundle> > v1(line 89)
BB22
39   v33 = invokevirtual < Application, Ljava/util/ResourceBundle, getLocale()Ljava/util/Locale; > v31 @82 exception:v32(line 89)
BB23
40   putfield v1 = v33 < Application, Lorg/apache/catalina/tribes/util/StringManager, locale, <Application,Ljava/util/Locale> >(line 89)
BB24
41   return                                  (line 91)
BB25

**CGNode:** Node: < Application, Lorg/apache/catalina/tribes/util/Arrays, toString([BIIZ)Ljava/lang/String; > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/membership/MemberImpl, <clinit>()V >:NEW <Primordial,[B>@15 in Everywhere} ]
**IR:** < Application, Lorg/apache/catalina/tribes/util/Arrays, toString([BIIZ)Ljava/lang/String; >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..0]
    -> BB2
    -> BB26
BB2[1..3]
    -> BB3
    -> BB26
BB3[4..7]
    -> BB23
    -> BB4
BB4[8..10]
    -> BB23
    -> BB5
BB5[11..15]
    -> BB15
    -> BB6
BB6[16..23]
    -> BB7
    -> BB26
BB7[24..26]
    -> BB8
    -> BB26
BB8[27..28]
    -> BB13
BB9[29..31]
    -> BB10
    -> BB26
BB10[32..34]
    -> BB11
    -> BB26
BB11[35..37]
    -> BB12
    -> BB26
BB12[38..42]
    -> BB13
BB13[43..45]
    -> BB9
    -> BB14
BB14[46..46]
    -> BB23
BB15[47..54]
    -> BB16
    -> BB26
BB16[55..55]
    -> BB17
    -> BB26
BB17[56..57]
    -> BB22
BB18[58..60]
    -> BB19
    -> BB26
BB19[61..63]
    -> BB20
    -> BB26
BB20[64..64]
    -> BB21
    -> BB26
BB21[65..69]
    -> BB22
BB22[70..72]
    -> BB18
    -> BB23
BB23[73..75]
    -> BB24
    -> BB26
BB24[76..78]
    -> BB25
    -> BB26
BB25[79..79]
    -> BB26
BB26[-1..-2]
Instructions:
BB0
BB1
0   v6 = new <Application,Ljava/lang/StringBuilder>@0(line 62)
BB2
3   invokespecial < Application, Ljava/lang/StringBuilder, <init>(Ljava/lang/String;)V > v6,v7:#{ @6 exception:v8(line 62)
BB3
7   conditional branch(eq) v1,v9:#null       (line 63)
BB4
10   conditional branch(le) v3,v10:#0        (line 63)
BB5
15   conditional branch(eq) v4,v10:#0        (line 65)
BB6
21   v24 = binaryop(add) v2 , v11:#1         (line 66)
23   v25 = arrayload v1[v2]                  (line 66)
BB7
25   v27 = binaryop(and) v25 , v26:#255      (line 66)
26   v29 = invokevirtual < Application, Ljava/lang/StringBuilder, append(I)Ljava/lang/StringBuilder; > v6,v27 @39 exception:v28(line 66)
BB8
28   goto                                    (line 67)
BB9
31   v31 = invokevirtual < Application, Ljava/lang/StringBuilder, append(Ljava/lang/String;)Ljava/lang/StringBuilder; > v6,v16:#,  @50 exception:v30(line 68)
BB10
34   v32 = arrayload v1[v37]                 (line 68)
BB11
36   v33 = binaryop(and) v32 , v26:#255      (line 68)
37   v35 = invokevirtual < Application, Ljava/lang/StringBuilder, append(I)Ljava/lang/StringBuilder; > v31,v33 @61 exception:v34(line 68)
BB12
41   v36 = binaryop(add) v37 , v11:#1        (line 67)
BB13
           v37 = phi  v24,v36
45   conditional branch(lt) v37,v3           (line 67)
BB14
46   goto                                    (line 67)
BB15
52   v12 = binaryop(add) v2 , v11:#1         (line 71)
54   v13 = arrayload v1[v2]                  (line 71)
BB16
55   v15 = invokevirtual < Application, Ljava/lang/StringBuilder, append(I)Ljava/lang/StringBuilder; > v6,v13 @86 exception:v14(line 71)
BB17
57   goto                                    (line 72)
BB18
60   v18 = invokevirtual < Application, Ljava/lang/StringBuilder, append(Ljava/lang/String;)Ljava/lang/StringBuilder; > v6,v16:#,  @97 exception:v17(line 73)
BB19
63   v19 = arrayload v1[v23]                 (line 73)
BB20
64   v21 = invokevirtual < Application, Ljava/lang/StringBuilder, append(I)Ljava/lang/StringBuilder; > v18,v19 @104 exception:v20(line 73)
BB21
68   v22 = binaryop(add) v23 , v11:#1        (line 72)
BB22
           v23 = phi  v12,v22
72   conditional branch(lt) v23,v3           (line 72)
BB23
75   v41 = invokevirtual < Application, Ljava/lang/StringBuilder, append(Ljava/lang/String;)Ljava/lang/StringBuilder; > v6,v39:#} @121 exception:v40(line 77)
BB24
78   v43 = invokevirtual < Application, Ljava/lang/StringBuilder, toString()Ljava/lang/String; > v6 @127 exception:v42(line 78)
BB25
79   return v43                              (line 78)
BB26

**CGNode:** Node: < Application, Lorg/apache/catalina/tribes/util/Arrays, toString([BIIZ)Ljava/lang/String; > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/membership/MemberImpl, <clinit>()V >:NEW <Primordial,[B>@69 in Everywhere} ]
**IR:** < Application, Lorg/apache/catalina/tribes/util/Arrays, toString([BIIZ)Ljava/lang/String; >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..0]
    -> BB2
    -> BB26
BB2[1..3]
    -> BB3
    -> BB26
BB3[4..7]
    -> BB23
    -> BB4
BB4[8..10]
    -> BB23
    -> BB5
BB5[11..15]
    -> BB15
    -> BB6
BB6[16..23]
    -> BB7
    -> BB26
BB7[24..26]
    -> BB8
    -> BB26
BB8[27..28]
    -> BB13
BB9[29..31]
    -> BB10
    -> BB26
BB10[32..34]
    -> BB11
    -> BB26
BB11[35..37]
    -> BB12
    -> BB26
BB12[38..42]
    -> BB13
BB13[43..45]
    -> BB9
    -> BB14
BB14[46..46]
    -> BB23
BB15[47..54]
    -> BB16
    -> BB26
BB16[55..55]
    -> BB17
    -> BB26
BB17[56..57]
    -> BB22
BB18[58..60]
    -> BB19
    -> BB26
BB19[61..63]
    -> BB20
    -> BB26
BB20[64..64]
    -> BB21
    -> BB26
BB21[65..69]
    -> BB22
BB22[70..72]
    -> BB18
    -> BB23
BB23[73..75]
    -> BB24
    -> BB26
BB24[76..78]
    -> BB25
    -> BB26
BB25[79..79]
    -> BB26
BB26[-1..-2]
Instructions:
BB0
BB1
0   v6 = new <Application,Ljava/lang/StringBuilder>@0(line 62)
BB2
3   invokespecial < Application, Ljava/lang/StringBuilder, <init>(Ljava/lang/String;)V > v6,v7:#{ @6 exception:v8(line 62)
BB3
7   conditional branch(eq) v1,v9:#null       (line 63)
BB4
10   conditional branch(le) v3,v10:#0        (line 63)
BB5
15   conditional branch(eq) v4,v10:#0        (line 65)
BB6
21   v24 = binaryop(add) v2 , v11:#1         (line 66)
23   v25 = arrayload v1[v2]                  (line 66)
BB7
25   v27 = binaryop(and) v25 , v26:#255      (line 66)
26   v29 = invokevirtual < Application, Ljava/lang/StringBuilder, append(I)Ljava/lang/StringBuilder; > v6,v27 @39 exception:v28(line 66)
BB8
28   goto                                    (line 67)
BB9
31   v31 = invokevirtual < Application, Ljava/lang/StringBuilder, append(Ljava/lang/String;)Ljava/lang/StringBuilder; > v6,v16:#,  @50 exception:v30(line 68)
BB10
34   v32 = arrayload v1[v37]                 (line 68)
BB11
36   v33 = binaryop(and) v32 , v26:#255      (line 68)
37   v35 = invokevirtual < Application, Ljava/lang/StringBuilder, append(I)Ljava/lang/StringBuilder; > v31,v33 @61 exception:v34(line 68)
BB12
41   v36 = binaryop(add) v37 , v11:#1        (line 67)
BB13
           v37 = phi  v24,v36
45   conditional branch(lt) v37,v3           (line 67)
BB14
46   goto                                    (line 67)
BB15
52   v12 = binaryop(add) v2 , v11:#1         (line 71)
54   v13 = arrayload v1[v2]                  (line 71)
BB16
55   v15 = invokevirtual < Application, Ljava/lang/StringBuilder, append(I)Ljava/lang/StringBuilder; > v6,v13 @86 exception:v14(line 71)
BB17
57   goto                                    (line 72)
BB18
60   v18 = invokevirtual < Application, Ljava/lang/StringBuilder, append(Ljava/lang/String;)Ljava/lang/StringBuilder; > v6,v16:#,  @97 exception:v17(line 73)
BB19
63   v19 = arrayload v1[v23]                 (line 73)
BB20
64   v21 = invokevirtual < Application, Ljava/lang/StringBuilder, append(I)Ljava/lang/StringBuilder; > v18,v19 @104 exception:v20(line 73)
BB21
68   v22 = binaryop(add) v23 , v11:#1        (line 72)
BB22
           v23 = phi  v12,v22
72   conditional branch(lt) v23,v3           (line 72)
BB23
75   v41 = invokevirtual < Application, Ljava/lang/StringBuilder, append(Ljava/lang/String;)Ljava/lang/StringBuilder; > v6,v39:#} @121 exception:v40(line 77)
BB24
78   v43 = invokevirtual < Application, Ljava/lang/StringBuilder, toString()Ljava/lang/String; > v6 @127 exception:v42(line 78)
BB25
79   return v43                              (line 78)
BB26

**CGNode:** Node: < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, getServiceStartTime()J > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/membership/MemberImpl, getMember([BII)Lorg/apache/catalina/tribes/membership/MemberImpl; >:NEW <Application,Lorg/apache/catalina/tribes/membership/MemberImpl>@3 in ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, main([Ljava/lang/String;)V >:NEW <Application,Lorg/apache/catalina/tribes/io/XByteBuffer>@19 in ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,[Ljava/lang/String>@1 in Everywhere} ]} ]} ]
**IR:** < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, getServiceStartTime()J >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..1]
    -> BB2
    -> BB3
BB2[2..2]
    -> BB3
BB3[-1..-2]
Instructions:
BB0
BB1
1   v3 = getfield < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, serviceStartTime, <Primordial,J> > v1(line 479)
BB2
2   return v3                                (line 479)
BB3

**CGNode:** Node: < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, toBytes(J[BI)[B > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/membership/MemberImpl, getMember([BII)Lorg/apache/catalina/tribes/membership/MemberImpl; >:NEW <Application,Lorg/apache/catalina/tribes/membership/MemberImpl>@3 in ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, main([Ljava/lang/String;)V >:NEW <Application,Lorg/apache/catalina/tribes/io/XByteBuffer>@19 in ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,[Ljava/lang/String>@1 in Everywhere} ]} ]} ]
**IR:** < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, toBytes(J[BI)[B >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..7]
    -> BB2
    -> BB10
BB2[8..19]
    -> BB3
    -> BB10
BB3[20..31]
    -> BB4
    -> BB10
BB4[32..43]
    -> BB5
    -> BB10
BB5[44..55]
    -> BB6
    -> BB10
BB6[56..67]
    -> BB7
    -> BB10
BB7[68..79]
    -> BB8
    -> BB10
BB8[80..91]
    -> BB9
    -> BB10
BB9[92..93]
    -> BB10
BB10[-1..-2]
Instructions:
BB0
BB1
3   v6 = binaryop(add) v3 , v5:#7            (line 483)
5   v7 = conversion(I) v1                    (line 483)
6   v8 = conversion(B) v7                    (line 483)
7   arraystore v2[v6] = v8                   (line 483)
BB2
10   v10 = binaryop(USHR) v1 , v9:#8         (line 484)
15   v12 = binaryop(add) v3 , v11:#6         (line 485)
17   v13 = conversion(I) v10                 (line 485)
18   v14 = conversion(B) v13                 (line 485)
19   arraystore v2[v12] = v14                (line 485)
BB3
22   v15 = binaryop(USHR) v10 , v9:#8        (line 486)
27   v17 = binaryop(add) v3 , v16:#5         (line 487)
29   v18 = conversion(I) v15                 (line 487)
30   v19 = conversion(B) v18                 (line 487)
31   arraystore v2[v17] = v19                (line 487)
BB4
34   v20 = binaryop(USHR) v15 , v9:#8        (line 488)
39   v22 = binaryop(add) v3 , v21:#4         (line 489)
41   v23 = conversion(I) v20                 (line 489)
42   v24 = conversion(B) v23                 (line 489)
43   arraystore v2[v22] = v24                (line 489)
BB5
46   v25 = binaryop(USHR) v20 , v9:#8        (line 490)
51   v27 = binaryop(add) v3 , v26:#3         (line 491)
53   v28 = conversion(I) v25                 (line 491)
54   v29 = conversion(B) v28                 (line 491)
55   arraystore v2[v27] = v29                (line 491)
BB6
58   v30 = binaryop(USHR) v25 , v9:#8        (line 492)
63   v32 = binaryop(add) v3 , v31:#2         (line 493)
65   v33 = conversion(I) v30                 (line 493)
66   v34 = conversion(B) v33                 (line 493)
67   arraystore v2[v32] = v34                (line 493)
BB7
70   v35 = binaryop(USHR) v30 , v9:#8        (line 494)
75   v37 = binaryop(add) v3 , v36:#1         (line 495)
77   v38 = conversion(I) v35                 (line 495)
78   v39 = conversion(B) v38                 (line 495)
79   arraystore v2[v37] = v39                (line 495)
BB8
82   v40 = binaryop(USHR) v35 , v9:#8        (line 496)
87   v42 = binaryop(add) v3 , v41:#0         (line 497)
89   v43 = conversion(I) v40                 (line 497)
90   v44 = conversion(B) v43                 (line 497)
91   arraystore v2[v42] = v44                (line 497)
BB9
93   return v2                               (line 498)
BB10

**CGNode:** Node: < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, getDataLength()I > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/membership/MemberImpl, getMember([BII)Lorg/apache/catalina/tribes/membership/MemberImpl; >:NEW <Application,Lorg/apache/catalina/tribes/membership/MemberImpl>@3 in ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, main([Ljava/lang/String;)V >:NEW <Application,Lorg/apache/catalina/tribes/io/XByteBuffer>@19 in ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,[Ljava/lang/String>@1 in Everywhere} ]} ]} ]
**IR:** < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, getDataLength()I >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..1]
    -> BB2
    -> BB12
BB2[2..15]
    -> BB3
    -> BB12
BB3[16..16]
    -> BB4
    -> BB12
BB4[17..21]
    -> BB5
    -> BB12
BB5[22..22]
    -> BB6
    -> BB12
BB6[23..27]
    -> BB7
    -> BB12
BB7[28..28]
    -> BB8
    -> BB12
BB8[29..35]
    -> BB9
    -> BB12
BB9[36..36]
    -> BB10
    -> BB12
BB10[37..39]
    -> BB11
    -> BB12
BB11[40..41]
    -> BB12
BB12[-1..-2]
Instructions:
BB0
BB1
0   v3 = getstatic < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, TRIBES_MBR_BEGIN, <Primordial,[B> >(line 185)
1   v4 = arraylength v3                      (line 185)
BB2
3   v6 = binaryop(add) v4 , v5:#4            (line 185)
5   v8 = binaryop(add) v6 , v7:#8            (line 185)
7   v9 = binaryop(add) v8 , v5:#4            (line 185)
9   v10 = binaryop(add) v9 , v5:#4           (line 185)
11   v11 = binaryop(add) v10 , v5:#4         (line 185)
13   v13 = binaryop(add) v11 , v12:#1        (line 185)
15   v14 = getfield < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, host, <Primordial,[B> > v1(line 192)
BB3
16   v15 = arraylength v14                   (line 192)
BB4
17   v16 = binaryop(add) v13 , v15           (line 185)
19   v17 = binaryop(add) v16 , v5:#4         (line 185)
21   v18 = getfield < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, command, <Primordial,[B> > v1(line 194)
BB5
22   v19 = arraylength v18                   (line 194)
BB6
23   v20 = binaryop(add) v17 , v19           (line 185)
25   v21 = binaryop(add) v20 , v5:#4         (line 185)
27   v22 = getfield < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, domain, <Primordial,[B> > v1(line 196)
BB7
28   v23 = arraylength v22                   (line 196)
BB8
29   v24 = binaryop(add) v21 , v23           (line 185)
31   v26 = binaryop(add) v24 , v25:#16       (line 185)
33   v27 = binaryop(add) v26 , v5:#4         (line 185)
35   v28 = getfield < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, payload, <Primordial,[B> > v1(line 199)
BB9
36   v29 = arraylength v28                   (line 199)
BB10
37   v30 = binaryop(add) v27 , v29           (line 185)
38   v31 = getstatic < Application, Lorg/apache/catalina/tribes/membership/MemberImpl, TRIBES_MBR_END, <Primordial,[B> >(line 200)
39   v32 = arraylength v31                   (line 200)
BB11
40   v33 = binaryop(add) v30 , v32           (line 185)
41   return v33                              (line 185)
BB12

**CGNode:** Node: < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, toBytes(I[BI)[B > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/membership/MemberImpl, getMember([BII)Lorg/apache/catalina/tribes/membership/MemberImpl; >:NEW <Application,Lorg/apache/catalina/tribes/membership/MemberImpl>@3 in ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, main([Ljava/lang/String;)V >:NEW <Application,Lorg/apache/catalina/tribes/io/XByteBuffer>@19 in ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,[Ljava/lang/String>@1 in Everywhere} ]} ]} ]
**IR:** < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, toBytes(I[BI)[B >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..6]
    -> BB2
    -> BB6
BB2[7..17]
    -> BB3
    -> BB6
BB3[18..28]
    -> BB4
    -> BB6
BB4[29..39]
    -> BB5
    -> BB6
BB5[40..41]
    -> BB6
BB6[-1..-2]
Instructions:
BB0
BB1
3   v6 = binaryop(add) v3 , v5:#3            (line 462)
5   v7 = conversion(B) v1                    (line 462)
6   arraystore v2[v6] = v7                   (line 462)
BB2
9   v9 = binaryop(USHR) v1 , v8:#8           (line 463)
14   v11 = binaryop(add) v3 , v10:#2         (line 464)
16   v12 = conversion(B) v9                  (line 464)
17   arraystore v2[v11] = v12                (line 464)
BB3
20   v13 = binaryop(USHR) v9 , v8:#8         (line 465)
25   v15 = binaryop(add) v3 , v14:#1         (line 466)
27   v16 = conversion(B) v13                 (line 466)
28   arraystore v2[v15] = v16                (line 466)
BB4
31   v17 = binaryop(USHR) v13 , v8:#8        (line 467)
36   v19 = binaryop(add) v3 , v18:#0         (line 468)
38   v20 = conversion(B) v17                 (line 468)
39   arraystore v2[v19] = v20                (line 468)
BB5
41   return v2                               (line 469)
BB6

**CGNode:** Node: < Application, Lorg/apache/catalina/tribes/util/StringManager, getString(Ljava/lang/String;[Ljava/lang/Object;)Ljava/lang/String; > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/util/StringManager, getManager(Ljava/lang/String;)Lorg/apache/catalina/tribes/util/StringManager; >:NEW <Application,Lorg/apache/catalina/tribes/util/StringManager>@15 in ReceiverStringContext: [ [<Primordial,Ljava/lang/String>] ]} ]
**IR:** < Application, Lorg/apache/catalina/tribes/util/StringManager, getString(Ljava/lang/String;[Ljava/lang/Object;)Ljava/lang/String; >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..2]
    -> BB2
    -> BB13
BB2[3..6]
    -> BB4
    -> BB3
BB3[7..8]
    -> BB4
BB4[9..9]
    -> BB5
    -> BB13
BB5[10..12]
    -> BB6
    -> BB13
BB6[13..16]
    -> BB7
    -> BB13
BB7[17..17]
    -> BB8
    -> BB13
BB8[18..20]
    -> BB9
    -> BB13
BB9[21..22]
    -> BB10
    -> BB13
BB10[23..24]
    -> BB11
    -> BB13
BB11[25..25]
    -> BB12
    -> BB13
BB12[26..26]
    -> BB13
BB13[-1..-2]
Instructions:
BB0
BB1
2   v6 = invokevirtual < Application, Lorg/apache/catalina/tribes/util/StringManager, getString(Ljava/lang/String;)Ljava/lang/String; > v1,v2 @2 exception:v5(line 138)
BB2
6   conditional branch(ne) v6,v7:#null       (line 139)
BB3
BB4
           v8 = phi  v6,v2
9   v9 = new <Application,Ljava/text/MessageFormat>@12(line 143)
BB5
12   invokespecial < Application, Ljava/text/MessageFormat, <init>(Ljava/lang/String;)V > v9,v8 @17 exception:v10(line 143)
BB6
16   v11 = getfield < Application, Lorg/apache/catalina/tribes/util/StringManager, locale, <Application,Ljava/util/Locale> > v1(line 144)
BB7
17   invokevirtual < Application, Ljava/text/MessageFormat, setLocale(Ljava/util/Locale;)V > v9,v11 @28 exception:v12(line 144)
BB8
20   v13 = new <Application,Ljava/lang/StringBuffer>@34(line 145)
BB9
22   invokespecial < Application, Ljava/lang/StringBuffer, <init>()V > v13 @38 exception:v14(line 145)
BB10
24   v16 = invokevirtual < Application, Ljava/text/MessageFormat, format([Ljava/lang/Object;Ljava/lang/StringBuffer;Ljava/text/FieldPosition;)Ljava/lang/StringBuffer; > v9,v3,v13,v7:#null @42 exception:v15(line 145)
BB11
25   v18 = invokevirtual < Application, Ljava/lang/StringBuffer, toString()Ljava/lang/String; > v16 @45 exception:v17(line 145)
BB12
26   return v18                              (line 145)
BB13

**CGNode:** Node: < Application, Lorg/apache/catalina/tribes/io/BufferPool, getBuffer(IZ)Lorg/apache/catalina/tribes/io/XByteBuffer; > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/io/BufferPool, getBufferPool()Lorg/apache/catalina/tribes/io/BufferPool; >:NEW <Application,Lorg/apache/catalina/tribes/io/BufferPool>@136 in ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, main([Ljava/lang/String;)V >:NEW <Application,Lorg/apache/catalina/tribes/io/XByteBuffer>@19 in ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,[Ljava/lang/String>@1 in Everywhere} ]} ]} ]
**IR:** < Application, Lorg/apache/catalina/tribes/io/BufferPool, getBuffer(IZ)Lorg/apache/catalina/tribes/io/XByteBuffer; >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..1]
    -> BB2
    -> BB9
BB2[2..3]
    -> BB6
    -> BB3
BB3[4..5]
    -> BB4
    -> BB9
BB4[6..8]
    -> BB5
    -> BB9
BB5[9..9]
    -> BB9
BB6[10..10]
    -> BB7
    -> BB9
BB7[11..14]
    -> BB8
    -> BB9
BB8[15..15]
    -> BB9
BB9[-1..-2]
Instructions:
BB0
BB1
1   v5 = getfield < Application, Lorg/apache/catalina/tribes/io/BufferPool, pool, <Application,Lorg/apache/catalina/tribes/io/BufferPool$BufferPoolAPI> > v1(line 44)
BB2
3   conditional branch(eq) v5,v6:#null       (line 44)
BB3
5   v9 = getfield < Application, Lorg/apache/catalina/tribes/io/BufferPool, pool, <Application,Lorg/apache/catalina/tribes/io/BufferPool$BufferPoolAPI> > v1(line 44)
BB4
8   v11 = invokeinterface < Application, Lorg/apache/catalina/tribes/io/BufferPool$BufferPoolAPI, getBuffer(IZ)Lorg/apache/catalina/tribes/io/XByteBuffer; > v9,v2,v3 @13 exception:v10(line 44)
BB5
9   return v11                               (line 44)
BB6
10   v7 = new <Application,Lorg/apache/catalina/tribes/io/XByteBuffer>@19(line 45)
BB7
14   invokespecial < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, <init>(IZ)V > v7,v2,v3 @25 exception:v8(line 45)
BB8
15   return v7                               (line 45)
BB9

**CGNode:** Node: < Application, Lorg/apache/juli/logging/LogFactory, getInstance(Ljava/lang/Class;)Lorg/apache/juli/logging/Log; > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/juli/logging/LogFactory, <clinit>()V >:NEW <Application,Lorg/apache/juli/logging/LogFactory>@0 in Everywhere} ]
**IR:** < Application, Lorg/apache/juli/logging/LogFactory, getInstance(Ljava/lang/Class;)Lorg/apache/juli/logging/Log; >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..2]
    -> BB2
    -> BB4
BB2[3..3]
    -> BB3
    -> BB4
BB3[4..4]
    -> BB4
BB4[-1..-2]
Instructions:
BB0
BB1
2   v5 = invokevirtual < Application, Ljava/lang/Class, getName()Ljava/lang/String; > v2 @2 exception:v4(line 114)
BB2
3   v7 = invokevirtual < Application, Lorg/apache/juli/logging/LogFactory, getInstance(Ljava/lang/String;)Lorg/apache/juli/logging/Log; > v1,v5 @5 exception:v6(line 114)
BB3
4   return v7                                (line 114)
BB4

**CGNode:** Node: < Application, Lorg/apache/tomcat/util/net/AprEndpoint$Acceptor, run()V > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/tomcat/util/net/AprEndpoint, createAcceptor()Lorg/apache/tomcat/util/net/AbstractEndpoint$Acceptor; >:NEW <Application,Lorg/apache/tomcat/util/net/AprEndpoint$Acceptor>@0 in ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, main([Ljava/lang/String;)V >:NEW <Application,Lorg/apache/tomcat/util/net/AprEndpoint>@0 in ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,[Ljava/lang/String>@6 in Everywhere} ]} ]} ]
**IR:** < Application, Lorg/apache/tomcat/util/net/AprEndpoint$Acceptor, run()V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..2]
    -> BB58
BB2[3..5]
    -> BB3
    -> BB63
BB3[6..7]
    -> BB4
    -> BB5
    -> BB63
BB4[8..8]
    -> BB6
BB5[9..9]
    -> BB6
BB6[10..11]
    -> BB7
    -> BB63
BB7[12..12]
    -> BB8
    -> BB63
BB8[13..14]
    -> BB12
    -> BB9
BB9[15..16]
    -> BB10
    -> BB63
BB10[17..17]
    -> BB11
    -> BB63
BB11[18..19]
    -> BB2
    -> BB12
BB12[20..21]
    -> BB13
    -> BB63
BB13[22..22]
    -> BB14
    -> BB63
BB14[23..24]
    -> BB16
    -> BB15
BB15[25..25]
    -> BB61
BB16[26..28]
    -> BB17
    -> BB63
BB17[29..30]
    -> BB18
    -> BB41
BB18[31..31]
    -> BB19
    -> BB41
BB19[32..35]
    -> BB20
    -> BB23
BB20[36..36]
    -> BB21
    -> BB23
BB21[37..37]
    -> BB22
    -> BB23
    -> BB41
BB22[38..39]
    -> BB26
BB23[40..42]
    -> BB24
    -> BB41
BB24[43..44]
    -> BB25
    -> BB41
BB25[45..47]
    -> BB41
    -> BB63
BB26[48..51]
    -> BB27
    -> BB41
BB27[52..52]
    -> BB28
    -> BB41
BB28[53..54]
    -> BB38
    -> BB29
BB29[55..56]
    -> BB30
    -> BB41
BB30[57..57]
    -> BB31
    -> BB41
BB31[58..59]
    -> BB38
    -> BB32
BB32[60..61]
    -> BB33
    -> BB41
BB33[62..63]
    -> BB34
    -> BB41
BB34[64..65]
    -> BB58
    -> BB35
BB35[66..67]
    -> BB36
    -> BB41
BB36[68..69]
    -> BB37
    -> BB41
BB37[70..70]
    -> BB58
BB38[71..72]
    -> BB39
    -> BB41
BB39[73..74]
    -> BB40
    -> BB41
BB40[75..75]
    -> BB58
BB41[76..78]
    -> BB42
    -> BB63
BB42[79..80]
    -> BB43
    -> BB63
BB43[81..81]
    -> BB44
    -> BB63
BB44[82..83]
    -> BB58
    -> BB45
BB45[84..86]
    -> BB46
    -> BB63
BB46[87..91]
    -> BB56
    -> BB47
BB47[92..93]
    -> BB48
    -> BB63
BB48[94..96]
    -> BB49
    -> BB63
BB49[97..98]
    -> BB53
    -> BB50
BB50[99..100]
    -> BB51
    -> BB63
BB51[101..103]
    -> BB52
    -> BB63
BB52[104..104]
    -> BB58
BB53[105..106]
    -> BB54
    -> BB63
BB54[107..109]
    -> BB55
    -> BB63
BB55[110..110]
    -> BB58
BB56[111..112]
    -> BB57
    -> BB63
BB57[113..115]
    -> BB58
    -> BB63
BB58[116..117]
    -> BB59
    -> BB63
BB59[118..118]
    -> BB60
    -> BB63
BB60[119..120]
    -> BB6
    -> BB61
BB61[121..123]
    -> BB62
    -> BB63
BB62[124..124]
    -> BB63
BB63[-1..-2]
Instructions:
BB0
BB1
2   goto                                     (line 971)
BB2
4   v10 = getstatic < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint$Acceptor$AcceptorState, PAUSED, <Application,Lorg/apache/tomcat/util/net/AbstractEndpoint$Acceptor$AcceptorState> >(line 975)
5   putfield v1 = v10 < Application, Lorg/apache/tomcat/util/net/AprEndpoint$Acceptor, state, <Application,Lorg/apache/tomcat/util/net/AbstractEndpoint$Acceptor$AcceptorState> >(line 975)
BB3
7   invokestatic < Application, Ljava/lang/Thread, sleep(J)V > v11:#50 @15 exception:v12(line 977)
BB4
8   goto                                     (line 977)
BB5<Handler>
           v13 = getCaughtException 
BB6
           v50 = phi  v50,v48,v50
11   v6 = getfield < Application, Lorg/apache/tomcat/util/net/AprEndpoint$Acceptor, this$0, <Application,Lorg/apache/tomcat/util/net/AprEndpoint> > v1(line 974)
BB7
12   v7 = getfield < Application, Lorg/apache/tomcat/util/net/AprEndpoint, paused, <Primordial,Z> > v6(line 974)
BB8
14   conditional branch(eq) v7,v3:#0         (line 974)
BB9
16   v8 = getfield < Application, Lorg/apache/tomcat/util/net/AprEndpoint$Acceptor, this$0, <Application,Lorg/apache/tomcat/util/net/AprEndpoint> > v1(line 974)
BB10
17   v9 = getfield < Application, Lorg/apache/tomcat/util/net/AprEndpoint, running, <Primordial,Z> > v8(line 974)
BB11
19   conditional branch(ne) v9,v3:#0         (line 974)
BB12
21   v15 = getfield < Application, Lorg/apache/tomcat/util/net/AprEndpoint$Acceptor, this$0, <Application,Lorg/apache/tomcat/util/net/AprEndpoint> > v1(line 983)
BB13
22   v16 = getfield < Application, Lorg/apache/tomcat/util/net/AprEndpoint, running, <Primordial,Z> > v15(line 983)
BB14
24   conditional branch(ne) v16,v3:#0        (line 983)
BB15
25   goto                                    (line 984)
BB16
27   v17 = getstatic < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint$Acceptor$AcceptorState, RUNNING, <Application,Lorg/apache/tomcat/util/net/AbstractEndpoint$Acceptor$AcceptorState> >(line 986)
28   putfield v1 = v17 < Application, Lorg/apache/tomcat/util/net/AprEndpoint$Acceptor, state, <Application,Lorg/apache/tomcat/util/net/AbstractEndpoint$Acceptor$AcceptorState> >(line 986)
BB17
30   v18 = getfield < Application, Lorg/apache/tomcat/util/net/AprEndpoint$Acceptor, this$0, <Application,Lorg/apache/tomcat/util/net/AprEndpoint> > v1(line 990)
BB18
31   invokevirtual < Application, Lorg/apache/tomcat/util/net/AprEndpoint, countUpOrAwaitConnection()V > v18 @66 exception:v19(line 990)
BB19
35   v21 = getfield < Application, Lorg/apache/tomcat/util/net/AprEndpoint$Acceptor, this$0, <Application,Lorg/apache/tomcat/util/net/AprEndpoint> > v1(line 996)
BB20
36   v22 = getfield < Application, Lorg/apache/tomcat/util/net/AprEndpoint, serverSock, <Primordial,J> > v21(line 996)
BB21
37   v24 = invokestatic < Application, Lorg/apache/tomcat/jni/Socket, accept(J)J > v22 @78 exception:v23(line 996)
BB22
39   goto                                    (line 996)
BB23<Handler>
           v34 = getCaughtException 
42   v35 = getfield < Application, Lorg/apache/tomcat/util/net/AprEndpoint$Acceptor, this$0, <Application,Lorg/apache/tomcat/util/net/AprEndpoint> > v1(line 999)
BB24
44   v37 = invokevirtual < Application, Lorg/apache/tomcat/util/net/AprEndpoint, handleExceptionWithDelay(I)I > v35,v50 @92 exception:v36(line 999)
BB25
47   throw v34                               (line 1001)
BB26
51   v25 = getfield < Application, Lorg/apache/tomcat/util/net/AprEndpoint$Acceptor, this$0, <Application,Lorg/apache/tomcat/util/net/AprEndpoint> > v1(line 1006)
BB27
52   v26 = getfield < Application, Lorg/apache/tomcat/util/net/AprEndpoint, running, <Primordial,Z> > v25(line 1006)
BB28
54   conditional branch(eq) v26,v3:#0        (line 1006)
BB29
56   v27 = getfield < Application, Lorg/apache/tomcat/util/net/AprEndpoint$Acceptor, this$0, <Application,Lorg/apache/tomcat/util/net/AprEndpoint> > v1(line 1006)
BB30
57   v28 = getfield < Application, Lorg/apache/tomcat/util/net/AprEndpoint, paused, <Primordial,Z> > v27(line 1006)
BB31
59   conditional branch(ne) v28,v3:#0        (line 1006)
BB32
61   v29 = getfield < Application, Lorg/apache/tomcat/util/net/AprEndpoint$Acceptor, this$0, <Application,Lorg/apache/tomcat/util/net/AprEndpoint> > v1(line 1008)
BB33
63   v31 = invokevirtual < Application, Lorg/apache/tomcat/util/net/AprEndpoint, processSocketWithOptions(J)Z > v29,v24 @126 exception:v30(line 1008)
BB34
65   conditional branch(ne) v31,v3:#0        (line 1008)
BB35
67   v38 = getfield < Application, Lorg/apache/tomcat/util/net/AprEndpoint$Acceptor, this$0, <Application,Lorg/apache/tomcat/util/net/AprEndpoint> > v1(line 1010)
BB36
69   invokestatic < Application, Lorg/apache/tomcat/util/net/AprEndpoint, access$0(Lorg/apache/tomcat/util/net/AprEndpoint;J)V > v38,v24 @137 exception:v39(line 1010)
BB37
70   goto                                    (line 1010)
BB38
72   v40 = getfield < Application, Lorg/apache/tomcat/util/net/AprEndpoint$Acceptor, this$0, <Application,Lorg/apache/tomcat/util/net/AprEndpoint> > v1(line 1014)
BB39
74   invokestatic < Application, Lorg/apache/tomcat/util/net/AprEndpoint, access$0(Lorg/apache/tomcat/util/net/AprEndpoint;J)V > v40,v24 @148 exception:v41(line 1014)
BB40
75   goto                                    (line 1014)
BB41<Handler>
           v43 = phi  v50,v50,v50,v50,v50,v37,v3:#0,v3:#0,v3:#0,v3:#0,v3:#0,v3:#0,v3:#0,v3:#0,v3:#0,v3:#0
           v42 = getCaughtException 
78   invokestatic < Application, Lorg/apache/tomcat/util/ExceptionUtils, handleThrowable(Ljava/lang/Throwable;)V > v42 @156 exception:v45(line 1017)
BB42
80   v46 = getfield < Application, Lorg/apache/tomcat/util/net/AprEndpoint$Acceptor, this$0, <Application,Lorg/apache/tomcat/util/net/AprEndpoint> > v1(line 1018)
BB43
81   v47 = getfield < Application, Lorg/apache/tomcat/util/net/AprEndpoint, running, <Primordial,Z> > v46(line 1018)
BB44
83   conditional branch(eq) v47,v3:#0        (line 1018)
BB45
84   v51 = getstatic < Application, Lorg/apache/tomcat/util/net/AprEndpoint, sm, <Application,Lorg/apache/tomcat/util/res/StringManager> >(line 1019)
86   v54 = invokevirtual < Application, Lorg/apache/tomcat/util/res/StringManager, getString(Ljava/lang/String;)Ljava/lang/String; > v51,v52:#endpoint.accept.fail @174 exception:v53(line 1019)
BB46
89   v55 = instanceof v42 <Application,Lorg/apache/tomcat/jni/Error>(line 1020)
91   conditional branch(eq) v55,v3:#0        (line 1020)
BB47
93   v56 = checkcast <Application,Lorg/apache/tomcat/jni/Error>v42(line 1021)
BB48
96   v58 = invokevirtual < Application, Lorg/apache/tomcat/jni/Error, getError()I > v56 @193 exception:v57(line 1022)
BB49
98   conditional branch(ne) v58,v59:#233     (line 1022)
BB50
100   v60 = getfield < Application, Lorg/apache/tomcat/util/net/AprEndpoint$Acceptor, log, <Application,Lorg/apache/juli/logging/Log> > v1(line 1026)
BB51
103   invokeinterface < Application, Lorg/apache/juli/logging/Log, warn(Ljava/lang/Object;Ljava/lang/Throwable;)V > v60,v54,v42 @208 exception:v61(line 1026)
BB52
104   goto                                   (line 1026)
BB53
106   v65 = getfield < Application, Lorg/apache/tomcat/util/net/AprEndpoint$Acceptor, log, <Application,Lorg/apache/juli/logging/Log> > v1(line 1028)
BB54
109   invokeinterface < Application, Lorg/apache/juli/logging/Log, error(Ljava/lang/Object;Ljava/lang/Throwable;)V > v65,v54,v42 @222 exception:v66(line 1028)
BB55
110   goto                                   (line 1028)
BB56
112   v67 = getfield < Application, Lorg/apache/tomcat/util/net/AprEndpoint$Acceptor, log, <Application,Lorg/apache/juli/logging/Log> > v1(line 1031)
BB57
115   invokeinterface < Application, Lorg/apache/juli/logging/Log, error(Ljava/lang/Object;Ljava/lang/Throwable;)V > v67,v54,v42 @236 exception:v68(line 1031)
BB58
           v48 = phi  v3:#0,v3:#0,v3:#0,v3:#0,v43,v43,v43,v43
117   v4 = getfield < Application, Lorg/apache/tomcat/util/net/AprEndpoint$Acceptor, this$0, <Application,Lorg/apache/tomcat/util/net/AprEndpoint> > v1(line 971)
BB59
118   v5 = getfield < Application, Lorg/apache/tomcat/util/net/AprEndpoint, running, <Primordial,Z> > v4(line 971)
BB60
120   conditional branch(ne) v5,v3:#0        (line 971)
BB61
122   v73 = getstatic < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint$Acceptor$AcceptorState, ENDED, <Application,Lorg/apache/tomcat/util/net/AbstractEndpoint$Acceptor$AcceptorState> >(line 1037)
123   putfield v1 = v73 < Application, Lorg/apache/tomcat/util/net/AprEndpoint$Acceptor, state, <Application,Lorg/apache/tomcat/util/net/AbstractEndpoint$Acceptor$AcceptorState> >(line 1037)
BB62
124   return                                 (line 1038)
BB63

**CGNode:** Node: < Application, Lorg/apache/catalina/tribes/util/StringManager, getString(Ljava/lang/String;)Ljava/lang/String; > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/util/StringManager, getManager(Ljava/lang/String;)Lorg/apache/catalina/tribes/util/StringManager; >:NEW <Application,Lorg/apache/catalina/tribes/util/StringManager>@15 in ReceiverStringContext: [ [<Primordial,Ljava/lang/String>] ]} ]
**IR:** < Application, Lorg/apache/catalina/tribes/util/StringManager, getString(Ljava/lang/String;)Ljava/lang/String; >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..2]
    -> BB5
    -> BB2
BB2[3..5]
    -> BB3
    -> BB10
BB3[6..8]
    -> BB4
    -> BB10
BB4[9..9]
    -> BB10
BB5[10..13]
    -> BB6
    -> BB10
BB6[14..15]
    -> BB7
    -> BB8
    -> BB10
BB7[16..17]
    -> BB9
BB8[18..20]
    -> BB9
BB9[21..22]
    -> BB10
BB10[-1..-2]
Instructions:
BB0
BB1
2   conditional branch(ne) v2,v4:#null       (line 103)
BB2
5   v12 = new <Application,Ljava/lang/IllegalArgumentException>@7(line 106)
BB3
8   invokespecial < Application, Ljava/lang/IllegalArgumentException, <init>(Ljava/lang/String;)V > v12,v11:#key may not have a null value @12 exception:v13(line 106)
BB4
9   throw v12                                (line 106)
BB5
13   v5 = getfield < Application, Lorg/apache/catalina/tribes/util/StringManager, bundle, <Application,Ljava/util/ResourceBundle> > v1(line 112)
BB6
15   v7 = invokevirtual < Application, Ljava/util/ResourceBundle, getString(Ljava/lang/String;)Ljava/lang/String; > v5,v2 @23 exception:v6(line 112)
BB7
17   goto                                    (line 112)
BB8<Handler>
           v8 = getCaughtException 
BB9
           v10 = phi  v7,v4:#null
22   return v10                              (line 127)
BB10

**CGNode:** Node: < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, <init>(IZ)V > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/io/BufferPool, getBuffer(IZ)Lorg/apache/catalina/tribes/io/XByteBuffer; >:NEW <Application,Lorg/apache/catalina/tribes/io/XByteBuffer>@19 in ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/io/BufferPool, getBufferPool()Lorg/apache/catalina/tribes/io/BufferPool; >:NEW <Application,Lorg/apache/catalina/tribes/io/BufferPool>@136 in ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, main([Ljava/lang/String;)V >:NEW <Application,Lorg/apache/catalina/tribes/io/XByteBuffer>@19 in ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,[Ljava/lang/String>@1 in Everywhere} ]} ]} ]} ]
**IR:** < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, <init>(IZ)V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..1]
    -> BB2
    -> BB9
BB2[2..4]
    -> BB3
    -> BB9
BB3[5..7]
    -> BB4
    -> BB9
BB4[8..10]
    -> BB5
    -> BB9
BB5[11..13]
    -> BB6
    -> BB9
BB6[14..14]
    -> BB7
    -> BB9
BB7[15..17]
    -> BB8
    -> BB9
BB8[18..18]
    -> BB9
BB9[-1..-2]
Instructions:
BB0
BB1
1   invokespecial < Application, Ljava/lang/Object, <init>()V > v1 @1 exception:v5(line 88)
BB2
4   putfield v1 = v6:#null < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, buf, <Primordial,[B> >(line 67)
BB3
7   putfield v1 = v7:#0 < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, bufSize, <Primordial,I> >(line 72)
BB4
10   putfield v1 = v8:#1 < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, discard, <Primordial,Z> >(line 81)
BB5
13   v9 = new <Primordial,[B>@21v2           (line 89)
BB6
14   putfield v1 = v9 < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, buf, <Primordial,[B> >(line 89)
BB7
17   putfield v1 = v3 < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, discard, <Primordial,Z> >(line 90)
BB8
18   return                                  (line 91)
BB9

**CGNode:** Node: < Application, Lorg/apache/juli/logging/LogFactory, getInstance(Ljava/lang/String;)Lorg/apache/juli/logging/Log; > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/juli/logging/LogFactory, <clinit>()V >:NEW <Application,Lorg/apache/juli/logging/LogFactory>@0 in Everywhere} ]
**IR:** < Application, Lorg/apache/juli/logging/LogFactory, getInstance(Ljava/lang/String;)Lorg/apache/juli/logging/Log; >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..1]
    -> BB2
    -> BB3
BB2[2..2]
    -> BB3
BB3[-1..-2]
Instructions:
BB0
BB1
1   v5 = invokestatic < Application, Lorg/apache/juli/logging/DirectJDKLog, getInstance(Ljava/lang/String;)Lorg/apache/juli/logging/Log; > v2 @1 exception:v4(line 99)
BB2
2   return v5                                (line 99)
BB3

**CGNode:** Node: < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, countUpOrAwaitConnection()V > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, main([Ljava/lang/String;)V >:NEW <Application,Lorg/apache/tomcat/util/net/AprEndpoint>@0 in ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,[Ljava/lang/String>@6 in Everywhere} ]} ]
**IR:** < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, countUpOrAwaitConnection()V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..1]
    -> BB2
    -> BB5
BB2[2..5]
    -> BB4
    -> BB3
BB3[6..7]
    -> BB4
    -> BB5
BB4[8..8]
    -> BB5
BB5[-1..-2]
Instructions:
BB0
BB1
1   v3 = getfield < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, connectionLimitLatch, <Application,Lorg/apache/tomcat/util/threads/LimitLatch> > v1(line 678)
BB2
5   conditional branch(eq) v3,v4:#null       (line 679)
BB3
7   invokevirtual < Application, Lorg/apache/tomcat/util/threads/LimitLatch, countUpOrAwait()V > v3 @10 exception:v5(line 679)
BB4
8   return                                   (line 680)
BB5

**CGNode:** Node: < Application, Lorg/apache/tomcat/jni/Socket, accept(J)J > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/tomcat/util/net/AprEndpoint, createAcceptor()Lorg/apache/tomcat/util/net/AbstractEndpoint$Acceptor; >:NEW <Application,Lorg/apache/tomcat/util/net/AprEndpoint$Acceptor>@0 in ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, main([Ljava/lang/String;)V >:NEW <Application,Lorg/apache/tomcat/util/net/AprEndpoint>@0 in ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,[Ljava/lang/String>@6 in Everywhere} ]} ]} ]
**CGNode:** Node: < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, handleExceptionWithDelay(I)I > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, main([Ljava/lang/String;)V >:NEW <Application,Lorg/apache/tomcat/util/net/AprEndpoint>@0 in ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,[Ljava/lang/String>@6 in Everywhere} ]} ]
**IR:** < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, handleExceptionWithDelay(I)I >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..2]
    -> BB5
    -> BB2
BB2[3..5]
    -> BB3
    -> BB4
    -> BB10
BB3[6..6]
    -> BB5
BB4[7..7]
    -> BB5
BB5[8..10]
    -> BB7
    -> BB6
BB6[11..12]
    -> BB10
BB7[13..15]
    -> BB9
    -> BB8
BB8[16..19]
    -> BB10
BB9[20..21]
    -> BB10
BB10[-1..-2]
Instructions:
BB0
BB1
2   conditional branch(le) v2,v4:#0          (line 705)
BB2
4   v5 = conversion(J) v2                    (line 707)
5   invokestatic < Application, Ljava/lang/Thread, sleep(J)V > v5 @6 exception:v6(line 707)
BB3
6   goto                                     (line 707)
BB4<Handler>
           v7 = getCaughtException 
BB5
10   conditional branch(ne) v2,v4:#0         (line 715)
BB6
12   return v12:#50                          (line 716)
BB7
15   conditional branch(ge) v2,v9:#1600      (line 717)
BB8
18   v11 = binaryop(mul) v2 , v10:#2         (line 718)
19   return v11                              (line 718)
BB9
21   return v9:#1600                         (line 720)
BB10

**CGNode:** Node: < Application, Lorg/apache/tomcat/util/net/AprEndpoint, processSocketWithOptions(J)Z > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, main([Ljava/lang/String;)V >:NEW <Application,Lorg/apache/tomcat/util/net/AprEndpoint>@0 in ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,[Ljava/lang/String>@6 in Everywhere} ]} ]
**IR:** < Application, Lorg/apache/tomcat/util/net/AprEndpoint, processSocketWithOptions(J)Z >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..1]
    -> BB2
    -> BB17
BB2[2..3]
    -> BB21
    -> BB3
BB3[4..4]
    -> BB4
    -> BB17
BB4[5..7]
    -> BB5
    -> BB11
    -> BB17
BB5[8..8]
    -> BB6
    -> BB11
    -> BB17
BB6[9..11]
    -> BB7
    -> BB11
    -> BB17
BB7[12..12]
    -> BB8
    -> BB17
BB8[13..16]
    -> BB9
    -> BB11
    -> BB17
BB9[17..17]
    -> BB10
    -> BB11
    -> BB17
BB10[18..18]
    -> BB21
BB11[19..21]
    -> BB12
    -> BB22
BB12[22..24]
    -> BB13
    -> BB22
BB13[25..26]
    -> BB14
    -> BB22
BB14[27..27]
    -> BB15
    -> BB22
BB15[28..29]
    -> BB16
    -> BB22
BB16[30..31]
    -> BB22
BB17[32..34]
    -> BB18
    -> BB22
BB18[35..38]
    -> BB19
    -> BB22
BB19[39..40]
    -> BB20
    -> BB22
BB20[41..42]
    -> BB22
BB21[43..44]
    -> BB22
BB22[-1..-2]
Instructions:
BB0
BB1
1   v4 = getfield < Application, Lorg/apache/tomcat/util/net/AprEndpoint, running, <Primordial,Z> > v1(line 824)
BB2
3   conditional branch(eq) v4,v5:#0          (line 824)
BB3
4   v6 = new <Application,Lorg/apache/tomcat/util/net/SocketWrapper>@7(line 826)
BB4
7   v8 = invokestatic < Application, Ljava/lang/Long, valueOf(J)Ljava/lang/Long; > v2 @12 exception:v7(line 826)
BB5
8   invokespecial < Application, Lorg/apache/tomcat/util/net/SocketWrapper, <init>(Ljava/lang/Object;)V > v6,v8 @15 exception:v9(line 826)
BB6
11   v11 = invokevirtual < Application, Lorg/apache/tomcat/util/net/AprEndpoint, getExecutor()Ljava/util/concurrent/Executor; > v1 @20 exception:v10(line 827)
BB7
12   v12 = new <Application,Lorg/apache/tomcat/util/net/AprEndpoint$SocketWithOptionsProcessor>@23(line 827)
BB8
16   invokespecial < Application, Lorg/apache/tomcat/util/net/AprEndpoint$SocketWithOptionsProcessor, <init>(Lorg/apache/tomcat/util/net/AprEndpoint;Lorg/apache/tomcat/util/net/SocketWrapper;)V > v12,v1,v6 @29 exception:v13(line 827)
BB9
17   invokeinterface < Application, Ljava/util/concurrent/Executor, execute(Ljava/lang/Runnable;)V > v11,v12 @32 exception:v14(line 827)
BB10
18   goto                                    (line 827)
BB11<Handler>
           v23 = getCaughtException 
20   v24 = getstatic < Application, Lorg/apache/tomcat/util/net/AprEndpoint, log, <Application,Lorg/apache/juli/logging/Log> >(line 830)
21   v25 = new <Application,Ljava/lang/StringBuilder>@44(line 830)
BB12
24   invokespecial < Application, Ljava/lang/StringBuilder, <init>(Ljava/lang/String;)V > v25,v26:#Socket processing request was rejected for: @51 exception:v27(line 830)
BB13
26   v29 = invokevirtual < Application, Ljava/lang/StringBuilder, append(J)Ljava/lang/StringBuilder; > v25,v2 @55 exception:v28(line 830)
BB14
27   v31 = invokevirtual < Application, Ljava/lang/StringBuilder, toString()Ljava/lang/String; > v29 @58 exception:v30(line 830)
BB15
29   invokeinterface < Application, Lorg/apache/juli/logging/Log, warn(Ljava/lang/Object;Ljava/lang/Throwable;)V > v24,v31,v23 @62 exception:v32(line 830)
BB16
31   return v5:#0                            (line 831)
BB17<Handler>
           v15 = getCaughtException 
34   invokestatic < Application, Lorg/apache/tomcat/util/ExceptionUtils, handleThrowable(Ljava/lang/Throwable;)V > v15 @71 exception:v16(line 833)
BB18
35   v17 = getstatic < Application, Lorg/apache/tomcat/util/net/AprEndpoint, log, <Application,Lorg/apache/juli/logging/Log> >(line 836)
36   v18 = getstatic < Application, Lorg/apache/tomcat/util/net/AprEndpoint, sm, <Application,Lorg/apache/tomcat/util/res/StringManager> >(line 836)
38   v21 = invokevirtual < Application, Lorg/apache/tomcat/util/res/StringManager, getString(Ljava/lang/String;)Ljava/lang/String; > v18,v19:#endpoint.process.fail @83 exception:v20(line 836)
BB19
40   invokeinterface < Application, Lorg/apache/juli/logging/Log, error(Ljava/lang/Object;Ljava/lang/Throwable;)V > v17,v21,v15 @87 exception:v22(line 836)
BB20
42   return v5:#0                            (line 837)
BB21
44   return v33:#1                           (line 839)
BB22

**CGNode:** Node: < Application, Lorg/apache/tomcat/util/net/AprEndpoint, access$0(Lorg/apache/tomcat/util/net/AprEndpoint;J)V > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, main([Ljava/lang/String;)V >:NEW <Application,Lorg/apache/tomcat/util/net/AprEndpoint>@0 in ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,[Ljava/lang/String>@6 in Everywhere} ]} ]
**IR:** < Application, Lorg/apache/tomcat/util/net/AprEndpoint, access$0(Lorg/apache/tomcat/util/net/AprEndpoint;J)V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..2]
    -> BB2
    -> BB3
BB2[3..3]
    -> BB3
BB3[-1..-2]
Instructions:
BB0
BB1
2   invokespecial < Application, Lorg/apache/tomcat/util/net/AprEndpoint, destroySocket(J)V > v1,v2 @2 exception:v4(line 932)
BB2
3   return                                   (line 932)
BB3

**CGNode:** Node: < Application, Lorg/apache/tomcat/util/res/StringManager, getString(Ljava/lang/String;)Ljava/lang/String; > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/tomcat/util/res/StringManager, getManager(Ljava/lang/String;Ljava/util/Locale;)Lorg/apache/tomcat/util/res/StringManager; >:NEW <Application,Lorg/apache/tomcat/util/res/StringManager>@51 in ReceiverStringContext: [ [<Primordial,Ljava/lang/String>] ]} ]
**IR:** < Application, Lorg/apache/tomcat/util/res/StringManager, getString(Ljava/lang/String;)Ljava/lang/String; >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..2]
    -> BB5
    -> BB2
BB2[3..5]
    -> BB3
    -> BB12
BB3[6..8]
    -> BB4
    -> BB12
BB4[9..9]
    -> BB12
BB5[10..13]
    -> BB6
    -> BB12
BB6[14..15]
    -> BB11
    -> BB7
BB7[16..17]
    -> BB8
    -> BB12
BB8[18..19]
    -> BB9
    -> BB10
    -> BB12
BB9[20..21]
    -> BB11
BB10[22..24]
    -> BB11
BB11[25..26]
    -> BB12
BB12[-1..-2]
Instructions:
BB0
BB1
2   conditional branch(ne) v2,v4:#null       (line 107)
BB2
5   v13 = new <Application,Ljava/lang/IllegalArgumentException>@7(line 110)
BB3
8   invokespecial < Application, Ljava/lang/IllegalArgumentException, <init>(Ljava/lang/String;)V > v13,v12:#key may not have a null value @12 exception:v14(line 110)
BB4
9   throw v13                                (line 110)
BB5
13   v5 = getfield < Application, Lorg/apache/tomcat/util/res/StringManager, bundle, <Application,Ljava/util/ResourceBundle> > v1(line 117)
BB6
15   conditional branch(eq) v5,v4:#null      (line 117)
BB7
17   v6 = getfield < Application, Lorg/apache/tomcat/util/res/StringManager, bundle, <Application,Ljava/util/ResourceBundle> > v1(line 118)
BB8
19   v8 = invokevirtual < Application, Ljava/util/ResourceBundle, getString(Ljava/lang/String;)Ljava/lang/String; > v6,v2 @30 exception:v7(line 118)
BB9
21   goto                                    (line 118)
BB10<Handler>
           v9 = getCaughtException 
BB11
           v11 = phi  v4:#null,v8,v4:#null
26   return v11                              (line 135)
BB12

**CGNode:** Node: < Application, Lorg/apache/juli/logging/DirectJDKLog, getInstance(Ljava/lang/String;)Lorg/apache/juli/logging/Log; > Context: ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Ljava/lang/Class, getName()Ljava/lang/String; >:NEW <Primordial,Ljava/lang/String>@0 in JavaTypeContext<point: <Primordial,Ljava/lang/Class>>} ]
**IR:** < Application, Lorg/apache/juli/logging/DirectJDKLog, getInstance(Ljava/lang/String;)Lorg/apache/juli/logging/Log; >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..0]
    -> BB2
    -> BB4
BB2[1..3]
    -> BB3
    -> BB4
BB3[4..4]
    -> BB4
BB4[-1..-2]
Instructions:
BB0
BB1
0   v3 = new <Application,Lorg/apache/juli/logging/DirectJDKLog>@0(line 191)
BB2
3   invokespecial < Application, Lorg/apache/juli/logging/DirectJDKLog, <init>(Ljava/lang/String;)V > v3,v1 @5 exception:v4(line 191)
BB3
4   return v3                                (line 191)
BB4

**CGNode:** Node: < Application, Lorg/apache/juli/logging/DirectJDKLog, <clinit>()V > Context: Everywhere
**IR:** < Application, Lorg/apache/juli/logging/DirectJDKLog, <clinit>()V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..1]
    -> BB2
    -> BB26
BB2[2..3]
    -> BB25
    -> BB3
BB3[4..5]
    -> BB4
    -> BB26
BB4[6..7]
    -> BB25
    -> BB5
BB5[8..9]
    -> BB6
    -> BB8
BB6[10..10]
    -> BB7
    -> BB8
BB7[11..12]
    -> BB9
BB8[13..13]
    -> BB9
BB9[14..16]
    -> BB10
    -> BB24
BB10[17..17]
    -> BB11
    -> BB24
BB11[18..18]
    -> BB12
    -> BB24
BB12[19..19]
    -> BB13
    -> BB24
BB13[20..22]
    -> BB14
    -> BB24
BB14[23..25]
    -> BB15
    -> BB24
BB15[26..29]
    -> BB21
BB16[30..32]
    -> BB17
    -> BB24
BB17[33..35]
    -> BB20
    -> BB18
BB18[36..38]
    -> BB19
    -> BB24
BB19[39..40]
    -> BB20
    -> BB24
BB20[41..44]
    -> BB21
BB21[45..47]
    -> BB22
    -> BB24
BB22[48..48]
    -> BB16
    -> BB23
BB23[49..49]
    -> BB25
BB24[50..50]
    -> BB25
BB25[51..51]
    -> BB26
BB26[-1..-2]
Instructions:
BB0
BB1
1   v4 = invokestatic < Application, Ljava/lang/System, getProperty(Ljava/lang/String;)Ljava/lang/String; > v2:#java.util.logging.config.class @2 exception:v3(line 43)
BB2
3   conditional branch(ne) v4,v5:#null       (line 43)
BB3
5   v8 = invokestatic < Application, Ljava/lang/System, getProperty(Ljava/lang/String;)Ljava/lang/String; > v6:#java.util.logging.config.file @10 exception:v7(line 44)
BB4
7   conditional branch(ne) v8,v5:#null       (line 44)
BB5
9   v11 = invokestatic < Application, Ljava/lang/Class, forName(Ljava/lang/String;)Ljava/lang/Class; > v9:#org.apache.juli.JdkLoggerConfig @18 exception:v10(line 48)
BB6
10   v13 = invokevirtual < Application, Ljava/lang/Class, newInstance()Ljava/lang/Object; > v11 @21 exception:v12(line 48)
BB7
12   goto                                    (line 48)
BB8<Handler>
           v14 = getCaughtException 
BB9
16   v19 = invokestatic < Application, Ljava/lang/System, getProperty(Ljava/lang/String;Ljava/lang/String;)Ljava/lang/String; > v16:#org.apache.juli.formatter,v17:#java.util.logging.SimpleFormatter @33 exception:v18(line 52)
BB10
17   v21 = invokestatic < Application, Ljava/lang/Class, forName(Ljava/lang/String;)Ljava/lang/Class; > v19 @36 exception:v20(line 52)
BB11
18   v23 = invokevirtual < Application, Ljava/lang/Class, newInstance()Ljava/lang/Object; > v21 @39 exception:v22(line 52)
BB12
19   v24 = checkcast <Application,Ljava/util/logging/Formatter>v23(line 52)
BB13
22   v27 = invokestatic < Application, Ljava/util/logging/Logger, getLogger(Ljava/lang/String;)Ljava/util/logging/Logger; > v25:# @48 exception:v26(line 55)
BB14
25   v29 = invokevirtual < Application, Ljava/util/logging/Logger, getHandlers()[Ljava/util/logging/Handler; > v27 @53 exception:v28(line 56)
BB15
29   goto                                    (line 57)
BB16
32   v32 = arrayload v29[v38]                (line 59)
BB17
33   v33 = instanceof v32 <Application,Ljava/util/logging/ConsoleHandler>(line 59)
35   conditional branch(eq) v33,v30:#0       (line 59)
BB18
38   v34 = arrayload v29[v38]                (line 60)
BB19
40   invokevirtual < Application, Ljava/util/logging/Handler, setFormatter(Ljava/util/logging/Formatter;)V > v34,v24 @75 exception:v35(line 60)
BB20
43   v37 = binaryop(add) v38 , v36:#1        (line 57)
BB21
           v38 = phi  v30:#0,v37
47   v31 = arraylength v29                   (line 57)
BB22
48   conditional branch(lt) v38,v31          (line 57)
BB23
49   goto                                    (line 57)
BB24<Handler>
           v39 = getCaughtException 
BB25
51   return                                  (line 32)
BB26

**CGNode:** Node: < Application, Lorg/apache/tomcat/util/net/SocketWrapper, <init>(Ljava/lang/Object;)V > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/tomcat/util/net/AprEndpoint, processSocketWithOptions(J)Z >:NEW <Application,Lorg/apache/tomcat/util/net/SocketWrapper>@7 in ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, main([Ljava/lang/String;)V >:NEW <Application,Lorg/apache/tomcat/util/net/AprEndpoint>@0 in ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,[Ljava/lang/String>@6 in Everywhere} ]} ]} ]
**IR:** < Application, Lorg/apache/tomcat/util/net/SocketWrapper, <init>(Ljava/lang/Object;)V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..1]
    -> BB2
    -> BB11
BB2[2..4]
    -> BB3
    -> BB11
BB3[5..7]
    -> BB4
    -> BB11
BB4[8..10]
    -> BB5
    -> BB11
BB5[11..13]
    -> BB6
    -> BB11
BB6[14..16]
    -> BB7
    -> BB11
BB7[17..19]
    -> BB8
    -> BB11
BB8[20..22]
    -> BB9
    -> BB11
BB9[23..25]
    -> BB10
    -> BB11
BB10[26..26]
    -> BB11
BB11[-1..-2]
Instructions:
BB0
BB1
1   invokespecial < Application, Ljava/lang/Object, <init>()V > v1 @1 exception:v4(line 31)
BB2
4   putfield v1 = v5:#-1 < Application, Lorg/apache/tomcat/util/net/SocketWrapper, lastAccess, <Primordial,J> >(line 23)
BB3
7   putfield v1 = v5:#-1 < Application, Lorg/apache/tomcat/util/net/SocketWrapper, timeout, <Primordial,J> >(line 24)
BB4
10   putfield v1 = v6:#0 < Application, Lorg/apache/tomcat/util/net/SocketWrapper, error, <Primordial,Z> >(line 25)
BB5
13   putfield v1 = v7:#0 < Application, Lorg/apache/tomcat/util/net/SocketWrapper, lastRegistered, <Primordial,J> >(line 26)
BB6
16   putfield v1 = v8:#100 < Application, Lorg/apache/tomcat/util/net/SocketWrapper, keepAliveLeft, <Primordial,I> >(line 27)
BB7
19   putfield v1 = v6:#0 < Application, Lorg/apache/tomcat/util/net/SocketWrapper, async, <Primordial,Z> >(line 28)
BB8
22   putfield v1 = v6:#0 < Application, Lorg/apache/tomcat/util/net/SocketWrapper, keptAlive, <Primordial,Z> >(line 29)
BB9
25   putfield v1 = v2 < Application, Lorg/apache/tomcat/util/net/SocketWrapper, socket, <Application,Ljava/lang/Object> >(line 32)
BB10
26   return                                  (line 33)
BB11

**CGNode:** Node: < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, getExecutor()Ljava/util/concurrent/Executor; > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, main([Ljava/lang/String;)V >:NEW <Application,Lorg/apache/tomcat/util/net/AprEndpoint>@0 in ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,[Ljava/lang/String>@6 in Everywhere} ]} ]
**IR:** < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, getExecutor()Ljava/util/concurrent/Executor; >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..1]
    -> BB2
    -> BB3
BB2[2..2]
    -> BB3
BB3[-1..-2]
Instructions:
BB0
BB1
1   v3 = getfield < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, executor, <Application,Ljava/util/concurrent/Executor> > v1(line 181)
BB2
2   return v3                                (line 181)
BB3

**CGNode:** Node: < Application, Lorg/apache/tomcat/util/net/AprEndpoint$SocketWithOptionsProcessor, <init>(Lorg/apache/tomcat/util/net/AprEndpoint;Lorg/apache/tomcat/util/net/SocketWrapper;)V > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/tomcat/util/net/AprEndpoint, processSocketWithOptions(J)Z >:NEW <Application,Lorg/apache/tomcat/util/net/AprEndpoint$SocketWithOptionsProcessor>@23 in ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, main([Ljava/lang/String;)V >:NEW <Application,Lorg/apache/tomcat/util/net/AprEndpoint>@0 in ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,[Ljava/lang/String>@6 in Everywhere} ]} ]} ]
**IR:** < Application, Lorg/apache/tomcat/util/net/AprEndpoint$SocketWithOptionsProcessor, <init>(Lorg/apache/tomcat/util/net/AprEndpoint;Lorg/apache/tomcat/util/net/SocketWrapper;)V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..2]
    -> BB2
    -> BB6
BB2[3..4]
    -> BB3
    -> BB6
BB3[5..7]
    -> BB4
    -> BB6
BB4[8..10]
    -> BB5
    -> BB6
BB5[11..11]
    -> BB6
BB6[-1..-2]
Instructions:
BB0
BB1
2   putfield v1 = v2 < Application, Lorg/apache/tomcat/util/net/AprEndpoint$SocketWithOptionsProcessor, this$0, <Application,Lorg/apache/tomcat/util/net/AprEndpoint> >(line 1754)
BB2
4   invokespecial < Application, Ljava/lang/Object, <init>()V > v1 @6 exception:v5(line 1752)
BB3
7   putfield v1 = v6:#null < Application, Lorg/apache/tomcat/util/net/AprEndpoint$SocketWithOptionsProcessor, socket, <Application,Lorg/apache/tomcat/util/net/SocketWrapper> >(line 1749)
BB4
10   putfield v1 = v3 < Application, Lorg/apache/tomcat/util/net/AprEndpoint$SocketWithOptionsProcessor, socket, <Application,Lorg/apache/tomcat/util/net/SocketWrapper> >(line 1753)
BB5
11   return                                  (line 1753)
BB6

**CGNode:** Node: < Application, Lorg/apache/tomcat/util/ExceptionUtils, handleThrowable(Ljava/lang/Throwable;)V > Context: ReceiverStringContext: [ [<Primordial,Ljava/lang/OutOfMemoryError>] ]
**IR:** < Application, Lorg/apache/tomcat/util/ExceptionUtils, handleThrowable(Ljava/lang/Throwable;)V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..3]
    -> BB4
    -> BB2
BB2[4..5]
    -> BB3
    -> BB8
BB3[6..6]
    -> BB8
BB4[7..10]
    -> BB7
    -> BB5
BB5[11..12]
    -> BB6
    -> BB8
BB6[13..13]
    -> BB8
BB7[14..14]
    -> BB8
BB8[-1..-2]
Instructions:
BB0
BB1
1   v3 = instanceof v1 <Application,Ljava/lang/ThreadDeath>(line 33)
3   conditional branch(eq) v3,v4:#0          (line 33)
BB2
5   v7 = checkcast <Application,Ljava/lang/ThreadDeath>v1(line 34)
BB3
6   throw v7                                 (line 34)
BB4
8   v5 = instanceof v1 <Application,Ljava/lang/VirtualMachineError>(line 36)
10   conditional branch(eq) v5,v4:#0         (line 36)
BB5
12   v6 = checkcast <Application,Ljava/lang/VirtualMachineError>v1(line 37)
BB6
13   throw v6                                (line 37)
BB7
14   return                                  (line 40)
BB8

**CGNode:** Node: < Application, Lorg/apache/tomcat/util/ExceptionUtils, handleThrowable(Ljava/lang/Throwable;)V > Context: ReceiverStringContext: [ [<Primordial,Ljava/lang/ExceptionInInitializerError>] ]
**IR:** < Application, Lorg/apache/tomcat/util/ExceptionUtils, handleThrowable(Ljava/lang/Throwable;)V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..3]
    -> BB4
    -> BB2
BB2[4..5]
    -> BB3
    -> BB8
BB3[6..6]
    -> BB8
BB4[7..10]
    -> BB7
    -> BB5
BB5[11..12]
    -> BB6
    -> BB8
BB6[13..13]
    -> BB8
BB7[14..14]
    -> BB8
BB8[-1..-2]
Instructions:
BB0
BB1
1   v3 = instanceof v1 <Application,Ljava/lang/ThreadDeath>(line 33)
3   conditional branch(eq) v3,v4:#0          (line 33)
BB2
5   v7 = checkcast <Application,Ljava/lang/ThreadDeath>v1(line 34)
BB3
6   throw v7                                 (line 34)
BB4
8   v5 = instanceof v1 <Application,Ljava/lang/VirtualMachineError>(line 36)
10   conditional branch(eq) v5,v4:#0         (line 36)
BB5
12   v6 = checkcast <Application,Ljava/lang/VirtualMachineError>v1(line 37)
BB6
13   throw v6                                (line 37)
BB7
14   return                                  (line 40)
BB8

**CGNode:** Node: < Application, Lorg/apache/tomcat/util/net/AprEndpoint, destroySocket(J)V > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, main([Ljava/lang/String;)V >:NEW <Application,Lorg/apache/tomcat/util/net/AprEndpoint>@0 in ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,[Ljava/lang/String>@6 in Everywhere} ]} ]
**IR:** < Application, Lorg/apache/tomcat/util/net/AprEndpoint, destroySocket(J)V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..3]
    -> BB2
    -> BB4
BB2[4..4]
    -> BB3
    -> BB4
BB3[5..5]
    -> BB4
BB4[-1..-2]
Instructions:
BB0
BB1
3   v4 = getfield < Application, Lorg/apache/tomcat/util/net/AprEndpoint, running, <Primordial,Z> > v1(line 936)
BB2
4   invokespecial < Application, Lorg/apache/tomcat/util/net/AprEndpoint, destroySocket(JZ)V > v1,v2,v4 @6 exception:v5(line 936)
BB3
5   return                                   (line 937)
BB4

**CGNode:** Node: < Application, Lorg/apache/juli/logging/DirectJDKLog, <init>(Ljava/lang/String;)V > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/juli/logging/DirectJDKLog, getInstance(Ljava/lang/String;)Lorg/apache/juli/logging/Log; >:NEW <Application,Lorg/apache/juli/logging/DirectJDKLog>@0 in ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Ljava/lang/Class, getName()Ljava/lang/String; >:NEW <Primordial,Ljava/lang/String>@0 in JavaTypeContext<point: <Primordial,Ljava/lang/Class>>} ]} ]
**IR:** < Application, Lorg/apache/juli/logging/DirectJDKLog, <init>(Ljava/lang/String;)V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..1]
    -> BB2
    -> BB5
BB2[2..4]
    -> BB3
    -> BB5
BB3[5..5]
    -> BB4
    -> BB5
BB4[6..6]
    -> BB5
BB5[-1..-2]
Instructions:
BB0
BB1
1   invokespecial < Application, Ljava/lang/Object, <init>()V > v1 @1 exception:v4(line 70)
BB2
4   v6 = invokestatic < Application, Ljava/util/logging/Logger, getLogger(Ljava/lang/String;)Ljava/util/logging/Logger; > v2 @6 exception:v5(line 71)
BB3
5   putfield v1 = v6 < Application, Lorg/apache/juli/logging/DirectJDKLog, logger, <Application,Ljava/util/logging/Logger> >(line 71)
BB4
6   return                                   (line 72)
BB5

**CGNode:** Node: < Application, Lorg/apache/tomcat/util/net/AprEndpoint, destroySocket(JZ)V > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, main([Ljava/lang/String;)V >:NEW <Application,Lorg/apache/tomcat/util/net/AprEndpoint>@0 in ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,[Ljava/lang/String>@6 in Everywhere} ]} ]
**IR:** < Application, Lorg/apache/tomcat/util/net/AprEndpoint, destroySocket(JZ)V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..2]
    -> BB6
    -> BB2
BB2[3..7]
    -> BB6
    -> BB3
BB3[8..9]
    -> BB4
    -> BB7
BB4[10..11]
    -> BB5
    -> BB7
BB5[12..12]
    -> BB6
BB6[13..13]
    -> BB7
BB7[-1..-2]
Instructions:
BB0
BB1
2   conditional branch(eq) v3,v5:#0          (line 944)
BB2
5   v7 = compare v2,v6:#0 opcode=cmp         (line 944)
7   conditional branch(eq) v7,v5:#0          (line 944)
BB3
9   invokestatic < Application, Lorg/apache/tomcat/jni/Socket, destroy(J)V > v2 @11 exception:v8(line 945)
BB4
11   v10 = invokevirtual < Application, Lorg/apache/tomcat/util/net/AprEndpoint, countDownConnection()J > v1 @15 exception:v9(line 946)
BB5
BB6
13   return                                  (line 948)
BB7

**CGNode:** Node: < Application, Lorg/apache/tomcat/jni/Socket, destroy(J)V > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, main([Ljava/lang/String;)V >:NEW <Application,Lorg/apache/tomcat/util/net/AprEndpoint>@0 in ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,[Ljava/lang/String>@6 in Everywhere} ]} ]
**CGNode:** Node: < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, countDownConnection()J > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, main([Ljava/lang/String;)V >:NEW <Application,Lorg/apache/tomcat/util/net/AprEndpoint>@0 in ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,[Ljava/lang/String>@6 in Everywhere} ]} ]
**IR:** < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, countDownConnection()J >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..1]
    -> BB2
    -> BB9
BB2[2..5]
    -> BB8
    -> BB3
BB3[6..7]
    -> BB4
    -> BB9
BB4[8..13]
    -> BB7
    -> BB5
BB5[14..15]
    -> BB6
    -> BB9
BB6[16..17]
    -> BB7
    -> BB9
BB7[18..19]
    -> BB9
BB8[20..21]
    -> BB9
BB9[-1..-2]
Instructions:
BB0
BB1
1   v3 = getfield < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, connectionLimitLatch, <Application,Lorg/apache/tomcat/util/threads/LimitLatch> > v1(line 683)
BB2
5   conditional branch(eq) v3,v4:#null       (line 684)
BB3
7   v7 = invokevirtual < Application, Lorg/apache/tomcat/util/threads/LimitLatch, countDown()J > v3 @10 exception:v6(line 685)
BB4
11   v9 = compare v7,v8:#0 opcode=cmp        (line 686)
13   conditional branch(ge) v9,v10:#0        (line 686)
BB5
15   v12 = invokevirtual < Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, getLog()Lorg/apache/juli/logging/Log; > v1 @21 exception:v11(line 687)
BB6
17   invokeinterface < Application, Lorg/apache/juli/logging/Log, warn(Ljava/lang/Object;)V > v12,v13:#Incorrect connection count, multiple socket.close called on the same socket. @27 exception:v14(line 687)
BB7
19   return v7                               (line 689)
BB8
21   return v5:#-1                           (line 690)
BB9

**CGNode:** Node: < Application, Lorg/apache/tomcat/util/net/AprEndpoint, getLog()Lorg/apache/juli/logging/Log; > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/tomcat/util/net/AbstractEndpoint, main([Ljava/lang/String;)V >:NEW <Application,Lorg/apache/tomcat/util/net/AprEndpoint>@0 in ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,[Ljava/lang/String>@6 in Everywhere} ]} ]
**IR:** < Application, Lorg/apache/tomcat/util/net/AprEndpoint, getLog()Lorg/apache/juli/logging/Log; >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..1]
    -> BB2
BB2[-1..-2]
Instructions:
BB0
BB1
0   v3 = getstatic < Application, Lorg/apache/tomcat/util/net/AprEndpoint, log, <Application,Lorg/apache/juli/logging/Log> >(line 952)
1   return v3                                (line 952)
BB2

**CGNode:** Node: < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, getBytesDirect()[B > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/io/BufferPool, getBuffer(IZ)Lorg/apache/catalina/tribes/io/XByteBuffer; >:NEW <Application,Lorg/apache/catalina/tribes/io/XByteBuffer>@19 in ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/io/BufferPool, getBufferPool()Lorg/apache/catalina/tribes/io/BufferPool; >:NEW <Application,Lorg/apache/catalina/tribes/io/BufferPool>@136 in ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, main([Ljava/lang/String;)V >:NEW <Application,Lorg/apache/catalina/tribes/io/XByteBuffer>@19 in ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,[Ljava/lang/String>@1 in Everywhere} ]} ]} ]} ]
**IR:** < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, getBytesDirect()[B >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..1]
    -> BB2
    -> BB3
BB2[2..2]
    -> BB3
BB3[-1..-2]
Instructions:
BB0
BB1
1   v3 = getfield < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, buf, <Primordial,[B> > v1(line 125)
BB2
2   return v3                                (line 125)
BB3

**CGNode:** Node: < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, setLength(I)V > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/io/BufferPool, getBuffer(IZ)Lorg/apache/catalina/tribes/io/XByteBuffer; >:NEW <Application,Lorg/apache/catalina/tribes/io/XByteBuffer>@19 in ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/io/BufferPool, getBufferPool()Lorg/apache/catalina/tribes/io/BufferPool; >:NEW <Application,Lorg/apache/catalina/tribes/io/BufferPool>@136 in ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/catalina/tribes/test/transport/SocketTribesReceive, main([Ljava/lang/String;)V >:NEW <Application,Lorg/apache/catalina/tribes/io/XByteBuffer>@19 in ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Lcom/ibm/wala/FakeRootClass, fakeRootMethod()V >:NEW <Application,[Ljava/lang/String>@1 in Everywhere} ]} ]} ]} ]
**IR:** < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, setLength(I)V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..2]
    -> BB2
    -> BB9
BB2[3..3]
    -> BB3
    -> BB9
BB3[4..4]
    -> BB7
    -> BB4
BB4[5..5]
    -> BB5
    -> BB9
BB5[6..8]
    -> BB6
    -> BB9
BB6[9..9]
    -> BB9
BB7[10..12]
    -> BB8
    -> BB9
BB8[13..13]
    -> BB9
BB9[-1..-2]
Instructions:
BB0
BB1
2   v4 = getfield < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, buf, <Primordial,[B> > v1(line 110)
BB2
3   v5 = arraylength v4                      (line 110)
BB3
4   conditional branch(le) v2,v5             (line 110)
BB4
5   v6 = new <Application,Ljava/lang/ArrayIndexOutOfBoundsException>@9(line 110)
BB5
8   invokespecial < Application, Ljava/lang/ArrayIndexOutOfBoundsException, <init>(Ljava/lang/String;)V > v6,v7:#Size is larger than existing buffer. @15 exception:v8(line 110)
BB6
9   throw v6                                 (line 110)
BB7
12   putfield v1 = v2 < Application, Lorg/apache/catalina/tribes/io/XByteBuffer, bufSize, <Primordial,I> >(line 111)
BB8
13   return                                  (line 112)
BB9

**CGNode:** Node: < Application, Lorg/apache/juli/logging/DirectJDKLog, info(Ljava/lang/Object;)V > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/juli/logging/DirectJDKLog, getInstance(Ljava/lang/String;)Lorg/apache/juli/logging/Log; >:NEW <Application,Lorg/apache/juli/logging/DirectJDKLog>@0 in ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Ljava/lang/Class, getName()Ljava/lang/String; >:NEW <Primordial,Ljava/lang/String>@0 in JavaTypeContext<point: <Primordial,Ljava/lang/Class>>} ]} ]
**IR:** < Application, Lorg/apache/juli/logging/DirectJDKLog, info(Ljava/lang/Object;)V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..3]
    -> BB2
    -> BB4
BB2[4..5]
    -> BB3
    -> BB4
BB3[6..6]
    -> BB4
BB4[-1..-2]
Instructions:
BB0
BB1
1   v4 = getstatic < Application, Ljava/util/logging/Level, INFO, <Application,Ljava/util/logging/Level> >(line 126)
3   v6 = invokestatic < Application, Ljava/lang/String, valueOf(Ljava/lang/Object;)Ljava/lang/String; > v2 @5 exception:v5(line 126)
BB2
5   invokespecial < Application, Lorg/apache/juli/logging/DirectJDKLog, log(Ljava/util/logging/Level;Ljava/lang/String;Ljava/lang/Throwable;)V > v1,v4,v6,v7:#null @9 exception:v8(line 126)
BB3
6   return                                   (line 127)
BB4

**CGNode:** Node: < Application, Lorg/apache/juli/logging/DirectJDKLog, error(Ljava/lang/Object;Ljava/lang/Throwable;)V > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/juli/logging/DirectJDKLog, getInstance(Ljava/lang/String;)Lorg/apache/juli/logging/Log; >:NEW <Application,Lorg/apache/juli/logging/DirectJDKLog>@0 in ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Ljava/lang/Class, getName()Ljava/lang/String; >:NEW <Primordial,Ljava/lang/String>@0 in JavaTypeContext<point: <Primordial,Ljava/lang/Class>>} ]} ]
**IR:** < Application, Lorg/apache/juli/logging/DirectJDKLog, error(Ljava/lang/Object;Ljava/lang/Throwable;)V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..3]
    -> BB2
    -> BB4
BB2[4..5]
    -> BB3
    -> BB4
BB3[6..6]
    -> BB4
BB4[-1..-2]
Instructions:
BB0
BB1
1   v5 = getstatic < Application, Ljava/util/logging/Level, SEVERE, <Application,Ljava/util/logging/Level> >(line 151)
3   v7 = invokestatic < Application, Ljava/lang/String, valueOf(Ljava/lang/Object;)Ljava/lang/String; > v2 @5 exception:v6(line 151)
BB2
5   invokespecial < Application, Lorg/apache/juli/logging/DirectJDKLog, log(Ljava/util/logging/Level;Ljava/lang/String;Ljava/lang/Throwable;)V > v1,v5,v7,v3 @9 exception:v8(line 151)
BB3
6   return                                   (line 152)
BB4

**CGNode:** Node: < Application, Lorg/apache/juli/logging/DirectJDKLog, warn(Ljava/lang/Object;Ljava/lang/Throwable;)V > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/juli/logging/DirectJDKLog, getInstance(Ljava/lang/String;)Lorg/apache/juli/logging/Log; >:NEW <Application,Lorg/apache/juli/logging/DirectJDKLog>@0 in ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Ljava/lang/Class, getName()Ljava/lang/String; >:NEW <Primordial,Ljava/lang/String>@0 in JavaTypeContext<point: <Primordial,Ljava/lang/Class>>} ]} ]
**IR:** < Application, Lorg/apache/juli/logging/DirectJDKLog, warn(Ljava/lang/Object;Ljava/lang/Throwable;)V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..3]
    -> BB2
    -> BB4
BB2[4..5]
    -> BB3
    -> BB4
BB3[6..6]
    -> BB4
BB4[-1..-2]
Instructions:
BB0
BB1
1   v5 = getstatic < Application, Ljava/util/logging/Level, WARNING, <Application,Ljava/util/logging/Level> >(line 141)
3   v7 = invokestatic < Application, Ljava/lang/String, valueOf(Ljava/lang/Object;)Ljava/lang/String; > v2 @5 exception:v6(line 141)
BB2
5   invokespecial < Application, Lorg/apache/juli/logging/DirectJDKLog, log(Ljava/util/logging/Level;Ljava/lang/String;Ljava/lang/Throwable;)V > v1,v5,v7,v3 @9 exception:v8(line 141)
BB3
6   return                                   (line 142)
BB4

**CGNode:** Node: < Application, Lorg/apache/juli/logging/DirectJDKLog, debug(Ljava/lang/Object;Ljava/lang/Throwable;)V > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/juli/logging/DirectJDKLog, getInstance(Ljava/lang/String;)Lorg/apache/juli/logging/Log; >:NEW <Application,Lorg/apache/juli/logging/DirectJDKLog>@0 in ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Ljava/lang/Class, getName()Ljava/lang/String; >:NEW <Primordial,Ljava/lang/String>@0 in JavaTypeContext<point: <Primordial,Ljava/lang/Class>>} ]} ]
**IR:** < Application, Lorg/apache/juli/logging/DirectJDKLog, debug(Ljava/lang/Object;Ljava/lang/Throwable;)V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..3]
    -> BB2
    -> BB4
BB2[4..5]
    -> BB3
    -> BB4
BB3[6..6]
    -> BB4
BB4[-1..-2]
Instructions:
BB0
BB1
1   v5 = getstatic < Application, Ljava/util/logging/Level, FINE, <Application,Ljava/util/logging/Level> >(line 111)
3   v7 = invokestatic < Application, Ljava/lang/String, valueOf(Ljava/lang/Object;)Ljava/lang/String; > v2 @5 exception:v6(line 111)
BB2
5   invokespecial < Application, Lorg/apache/juli/logging/DirectJDKLog, log(Ljava/util/logging/Level;Ljava/lang/String;Ljava/lang/Throwable;)V > v1,v5,v7,v3 @9 exception:v8(line 111)
BB3
6   return                                   (line 112)
BB4

**CGNode:** Node: < Application, Lorg/apache/juli/logging/DirectJDKLog, isDebugEnabled()Z > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/juli/logging/DirectJDKLog, getInstance(Ljava/lang/String;)Lorg/apache/juli/logging/Log; >:NEW <Application,Lorg/apache/juli/logging/DirectJDKLog>@0 in ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Ljava/lang/Class, getName()Ljava/lang/String; >:NEW <Primordial,Ljava/lang/String>@0 in JavaTypeContext<point: <Primordial,Ljava/lang/Class>>} ]} ]
**IR:** < Application, Lorg/apache/juli/logging/DirectJDKLog, isDebugEnabled()Z >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..1]
    -> BB2
    -> BB4
BB2[2..3]
    -> BB3
    -> BB4
BB3[4..4]
    -> BB4
BB4[-1..-2]
Instructions:
BB0
BB1
1   v3 = getfield < Application, Lorg/apache/juli/logging/DirectJDKLog, logger, <Application,Ljava/util/logging/Logger> > v1(line 91)
BB2
2   v4 = getstatic < Application, Ljava/util/logging/Level, FINE, <Application,Ljava/util/logging/Level> >(line 91)
3   v6 = invokevirtual < Application, Ljava/util/logging/Logger, isLoggable(Ljava/util/logging/Level;)Z > v3,v4 @7 exception:v5(line 91)
BB3
4   return v6                                (line 91)
BB4

**CGNode:** Node: < Application, Lorg/apache/juli/logging/DirectJDKLog, warn(Ljava/lang/Object;)V > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/juli/logging/DirectJDKLog, getInstance(Ljava/lang/String;)Lorg/apache/juli/logging/Log; >:NEW <Application,Lorg/apache/juli/logging/DirectJDKLog>@0 in ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Ljava/lang/Class, getName()Ljava/lang/String; >:NEW <Primordial,Ljava/lang/String>@0 in JavaTypeContext<point: <Primordial,Ljava/lang/Class>>} ]} ]
**IR:** < Application, Lorg/apache/juli/logging/DirectJDKLog, warn(Ljava/lang/Object;)V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..3]
    -> BB2
    -> BB4
BB2[4..5]
    -> BB3
    -> BB4
BB3[6..6]
    -> BB4
BB4[-1..-2]
Instructions:
BB0
BB1
1   v4 = getstatic < Application, Ljava/util/logging/Level, WARNING, <Application,Ljava/util/logging/Level> >(line 136)
3   v6 = invokestatic < Application, Ljava/lang/String, valueOf(Ljava/lang/Object;)Ljava/lang/String; > v2 @5 exception:v5(line 136)
BB2
5   invokespecial < Application, Lorg/apache/juli/logging/DirectJDKLog, log(Ljava/util/logging/Level;Ljava/lang/String;Ljava/lang/Throwable;)V > v1,v4,v6,v7:#null @9 exception:v8(line 136)
BB3
6   return                                   (line 137)
BB4

**CGNode:** Node: < Application, Lorg/apache/juli/logging/DirectJDKLog, trace(Ljava/lang/Object;)V > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/juli/logging/DirectJDKLog, getInstance(Ljava/lang/String;)Lorg/apache/juli/logging/Log; >:NEW <Application,Lorg/apache/juli/logging/DirectJDKLog>@0 in ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Ljava/lang/Class, getName()Ljava/lang/String; >:NEW <Primordial,Ljava/lang/String>@0 in JavaTypeContext<point: <Primordial,Ljava/lang/Class>>} ]} ]
**IR:** < Application, Lorg/apache/juli/logging/DirectJDKLog, trace(Ljava/lang/Object;)V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..3]
    -> BB2
    -> BB4
BB2[4..5]
    -> BB3
    -> BB4
BB3[6..6]
    -> BB4
BB4[-1..-2]
Instructions:
BB0
BB1
1   v4 = getstatic < Application, Ljava/util/logging/Level, FINER, <Application,Ljava/util/logging/Level> >(line 116)
3   v6 = invokestatic < Application, Ljava/lang/String, valueOf(Ljava/lang/Object;)Ljava/lang/String; > v2 @5 exception:v5(line 116)
BB2
5   invokespecial < Application, Lorg/apache/juli/logging/DirectJDKLog, log(Ljava/util/logging/Level;Ljava/lang/String;Ljava/lang/Throwable;)V > v1,v4,v6,v7:#null @9 exception:v8(line 116)
BB3
6   return                                   (line 117)
BB4

**CGNode:** Node: < Application, Lorg/apache/juli/logging/DirectJDKLog, isTraceEnabled()Z > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/juli/logging/DirectJDKLog, getInstance(Ljava/lang/String;)Lorg/apache/juli/logging/Log; >:NEW <Application,Lorg/apache/juli/logging/DirectJDKLog>@0 in ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Ljava/lang/Class, getName()Ljava/lang/String; >:NEW <Primordial,Ljava/lang/String>@0 in JavaTypeContext<point: <Primordial,Ljava/lang/Class>>} ]} ]
**IR:** < Application, Lorg/apache/juli/logging/DirectJDKLog, isTraceEnabled()Z >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..1]
    -> BB2
    -> BB4
BB2[2..3]
    -> BB3
    -> BB4
BB3[4..4]
    -> BB4
BB4[-1..-2]
Instructions:
BB0
BB1
1   v3 = getfield < Application, Lorg/apache/juli/logging/DirectJDKLog, logger, <Application,Ljava/util/logging/Logger> > v1(line 101)
BB2
2   v4 = getstatic < Application, Ljava/util/logging/Level, FINER, <Application,Ljava/util/logging/Level> >(line 101)
3   v6 = invokevirtual < Application, Ljava/util/logging/Logger, isLoggable(Ljava/util/logging/Level;)Z > v3,v4 @7 exception:v5(line 101)
BB3
4   return v6                                (line 101)
BB4

**CGNode:** Node: < Application, Lorg/apache/juli/logging/DirectJDKLog, isInfoEnabled()Z > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/juli/logging/DirectJDKLog, getInstance(Ljava/lang/String;)Lorg/apache/juli/logging/Log; >:NEW <Application,Lorg/apache/juli/logging/DirectJDKLog>@0 in ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Ljava/lang/Class, getName()Ljava/lang/String; >:NEW <Primordial,Ljava/lang/String>@0 in JavaTypeContext<point: <Primordial,Ljava/lang/Class>>} ]} ]
**IR:** < Application, Lorg/apache/juli/logging/DirectJDKLog, isInfoEnabled()Z >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..1]
    -> BB2
    -> BB4
BB2[2..3]
    -> BB3
    -> BB4
BB3[4..4]
    -> BB4
BB4[-1..-2]
Instructions:
BB0
BB1
1   v3 = getfield < Application, Lorg/apache/juli/logging/DirectJDKLog, logger, <Application,Ljava/util/logging/Logger> > v1(line 86)
BB2
2   v4 = getstatic < Application, Ljava/util/logging/Level, INFO, <Application,Ljava/util/logging/Level> >(line 86)
3   v6 = invokevirtual < Application, Ljava/util/logging/Logger, isLoggable(Ljava/util/logging/Level;)Z > v3,v4 @7 exception:v5(line 86)
BB3
4   return v6                                (line 86)
BB4

**CGNode:** Node: < Application, Lorg/apache/juli/logging/DirectJDKLog, error(Ljava/lang/Object;)V > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/juli/logging/DirectJDKLog, getInstance(Ljava/lang/String;)Lorg/apache/juli/logging/Log; >:NEW <Application,Lorg/apache/juli/logging/DirectJDKLog>@0 in ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Ljava/lang/Class, getName()Ljava/lang/String; >:NEW <Primordial,Ljava/lang/String>@0 in JavaTypeContext<point: <Primordial,Ljava/lang/Class>>} ]} ]
**IR:** < Application, Lorg/apache/juli/logging/DirectJDKLog, error(Ljava/lang/Object;)V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..3]
    -> BB2
    -> BB4
BB2[4..5]
    -> BB3
    -> BB4
BB3[6..6]
    -> BB4
BB4[-1..-2]
Instructions:
BB0
BB1
1   v4 = getstatic < Application, Ljava/util/logging/Level, SEVERE, <Application,Ljava/util/logging/Level> >(line 146)
3   v6 = invokestatic < Application, Ljava/lang/String, valueOf(Ljava/lang/Object;)Ljava/lang/String; > v2 @5 exception:v5(line 146)
BB2
5   invokespecial < Application, Lorg/apache/juli/logging/DirectJDKLog, log(Ljava/util/logging/Level;Ljava/lang/String;Ljava/lang/Throwable;)V > v1,v4,v6,v7:#null @9 exception:v8(line 146)
BB3
6   return                                   (line 147)
BB4

**CGNode:** Node: < Application, Lorg/apache/juli/logging/DirectJDKLog, log(Ljava/util/logging/Level;Ljava/lang/String;Ljava/lang/Throwable;)V > Context: ReceiverStringContext: [ SITE_IN_NODE{< Application, Lorg/apache/juli/logging/DirectJDKLog, getInstance(Ljava/lang/String;)Lorg/apache/juli/logging/Log; >:NEW <Application,Lorg/apache/juli/logging/DirectJDKLog>@0 in ReceiverStringContext: [ SITE_IN_NODE{synthetic < Primordial, Ljava/lang/Class, getName()Ljava/lang/String; >:NEW <Primordial,Ljava/lang/String>@0 in JavaTypeContext<point: <Primordial,Ljava/lang/Class>>} ]} ]
**IR:** < Application, Lorg/apache/juli/logging/DirectJDKLog, log(Ljava/util/logging/Level;Ljava/lang/String;Ljava/lang/Throwable;)V >
CFG:
BB0[-1..-2]
    -> BB1
BB1[0..1]
    -> BB2
    -> BB21
BB2[2..3]
    -> BB3
    -> BB21
BB3[4..5]
    -> BB20
    -> BB4
BB4[6..6]
    -> BB5
    -> BB21
BB5[7..8]
    -> BB6
    -> BB21
BB6[9..11]
    -> BB7
    -> BB21
BB7[12..19]
    -> BB14
    -> BB8
BB8[20..21]
    -> BB9
    -> BB21
BB9[22..23]
    -> BB14
    -> BB10
BB10[24..26]
    -> BB11
    -> BB21
BB11[27..29]
    -> BB12
    -> BB21
BB12[30..32]
    -> BB13
    -> BB21
BB13[33..33]
    -> BB14
BB14[34..36]
    -> BB18
    -> BB15
BB15[37..38]
    -> BB16
    -> BB21
BB16[39..43]
    -> BB17
    -> BB21
BB17[44..44]
    -> BB20
BB18[45..46]
    -> BB19
    -> BB21
BB19[47..52]
    -> BB20
    -> BB21
BB20[53..53]
    -> BB21
BB21[-1..-2]
Instructions:
BB0
BB1
1   v6 = getfield < Application, Lorg/apache/juli/logging/DirectJDKLog, logger, <Application,Ljava/util/logging/Logger> > v1(line 170)
BB2
3   v8 = invokevirtual < Application, Ljava/util/logging/Logger, isLoggable(Ljava/util/logging/Level;)Z > v6,v2 @5 exception:v7(line 170)
BB3
5   conditional branch(eq) v8,v9:#0          (line 170)
BB4
6   v10 = new <Application,Ljava/lang/Throwable>@11(line 172)
BB5
8   invokespecial < Application, Ljava/lang/Throwable, <init>()V > v10 @15 exception:v11(line 172)
BB6
11   v13 = invokevirtual < Application, Ljava/lang/Throwable, getStackTrace()[Ljava/lang/StackTraceElement; > v10 @22 exception:v12(line 173)
BB7
19   conditional branch(eq) v13,v15:#null    (line 177)
BB8
21   v16 = arraylength v13                   (line 177)
BB9
23   conditional branch(le) v16,v17:#2       (line 177)
BB10
26   v18 = arrayload v13[v17:#2]             (line 178)
BB11
29   v20 = invokevirtual < Application, Ljava/lang/StackTraceElement, getClassName()Ljava/lang/String; > v18 @55 exception:v19(line 179)
BB12
32   v22 = invokevirtual < Application, Ljava/lang/StackTraceElement, getMethodName()Ljava/lang/String; > v18 @62 exception:v21(line 180)
BB13
BB14
           v23 = phi  v14:#unknown,v14:#unknown,v20
           v24 = phi  v14:#unknown,v14:#unknown,v22
36   conditional branch(ne) v4,v15:#null     (line 182)
BB15
38   v27 = getfield < Application, Lorg/apache/juli/logging/DirectJDKLog, logger, <Application,Ljava/util/logging/Logger> > v1(line 183)
BB16
43   invokevirtual < Application, Ljava/util/logging/Logger, logp(Ljava/util/logging/Level;Ljava/lang/String;Ljava/lang/String;Ljava/lang/String;)V > v27,v2,v23,v24,v3 @81 exception:v28(line 183)
BB17
44   goto                                    (line 183)
BB18
46   v25 = getfield < Application, Lorg/apache/juli/logging/DirectJDKLog, logger, <Application,Ljava/util/logging/Logger> > v1(line 185)
BB19
52   invokevirtual < Application, Ljava/util/logging/Logger, logp(Ljava/util/logging/Level;Ljava/lang/String;Ljava/lang/String;Ljava/lang/String;Ljava/lang/Throwable;)V > v25,v2,v23,v24,v3,v4 @98 exception:v26(line 185)
BB20
53   return                                  (line 188)
BB21

