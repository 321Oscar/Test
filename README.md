# Test
first repository
## DataGridView增加行数
在列头上绘制行数

Refactor my code, to make it more efficient and simple  
Reply with code and explanations and further suggestions.

```CSharp
public interface ICANController
    {
        bool IsOpen { get; set; }
        int DeviceType { get; set; }
        int DeviceInd { get; set; }
        int MaxDataCount { get; set; }
        bool Recv_Start { get; set; }
       
        bool Open();
        bool StartCan(int canindex);
        bool Close();
        bool Send(int canindex = 0, CANSendFrame sendData = null, byte sendtype = 0);
        CANReceiveFrame[] Receive(int[] ids, int canindex);
        CANReceiveFrame[] Receive(int canindex);
        void StartReceive(bool start, int[] canind);
        void RecvDataFunc();
        void Register(ReceiveDataEventHandler recieveMethod, int canChannel);
        void UnRegister(ReceiveDataEventHandler recieveMethod, int canChannel);
        void OnChannal0DataRecieved(CANDataReceiveEventArgs args);
        void OnChannal1DataRecieved(CANDataReceiveEventArgs args);
        ShowLog ShowlogEvent { get; set; }
        ShowLog SaveLog { get; set; }
    }

    public interface ICANControllerAdapter: ICANController
    {
        bool InitCan(params object[] param);
    }
```
## Record
