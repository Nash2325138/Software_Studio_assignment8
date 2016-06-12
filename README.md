# Software_Studio_assignment8
Just for hand in the assignment

這次的 assignment 是建立在之前 lab10 之上的作業，目的是要讓 lab10 簡易計算機的結果顯示在自己開的 java server 上面。

server端其實就是把助教提供的 socket example 的 receive socket thread 改成想顯示的形式。

手機 app 端是把 lab10 在 jumpToMainLayout() 之前多加一個 jumpToIPinputLayout()，並且在這個 layout 上面使用 EditText 把使用者輸入的 IP 存下來。
使用者輸入的 IP 並按下 OK button 後，就 jumpToMainLayout()，做跟 lab10 一樣的事。
之後在算出答案時，開一個 ResultSendThread 把答案字串透過 socket 傳到 server 那裡（透過之前得到的使用者輸入的 server IP，port 綁死為 2000）

這就是整個架構的粗略概念
