
0.��ز��ͣ�https://blog.csdn.net/shenshikexmu/article/details/80013444


1.�������ݣ�calfata.mat

2.����У���㷨
   [Ta,Ka,Ba,Tg,Kg,Bg,Tm2a,Bm,Vm,mag_strength]=ImuCalibration_Gesture(cal_data)


3.У�����֣�
   ���ٶȡ����ٶȣ�����ICRA2014���ģ�<A Robust and Easy to implement method for imu
                                   calibration without External Equipments>
   �����Ʋ��֣��㷨mag2acc_matrix����������������ļнǲ��䣬
              �㷨Cal_mag4acc_frame���ò�ͬ��̬�´��������ܵĴ�ͨ�����ı仯����̬�仯������ԣ����������

4.�������֣�
  cal_acc=Ta*Ka*(raw_acc+Ba)
  cal_gyro=Tg*Kg*(raw_gyro+Bg)
  cal_mag=Tm2a*(raw_mag+Bm)
   
5.��̬���֣�
   Mahony filter:
   conference <Nonlinear Complementery Filters on the Special Orthogonal Group>
   inspired by    http://blog.csdn.net/luoshi006/article/details/51513580
   EKF:
   derivation <A Double-Stage Kalman Filter for Orientation Tracking with 
               an Integrated Processor in 9-D IMU>
   high low pass:
   high and low pass filter to Gyro atitude with Accelerate & Magnetic
   

