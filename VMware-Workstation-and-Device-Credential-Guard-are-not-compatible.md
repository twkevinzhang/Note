# VMware-Workstation-and-Device-Credential-Guard-are-not-compatible

## 參考
 - https://codertw.com/程式語言/554123/

## 錯誤訊息
> VMware Workstation和Device / Credential Guard不相容。禁用Device / Credential Guard後，可以執行VMware Workstation。

## 原因
1. 出現此問題的原因是Device Guard或Credential Guard與Workstation不相容。
2. Windows系統的Hyper-V不相容導致。

## 解決方法

禁用用於啟用Credential Guard的組策略設定。

 - 在主機作業系統上，單擊"S tart" > "執行"，鍵入gpedit.msc，然後單擊" 確定"。本地組策略編輯器開啟。
 - 轉至本地計算機策略 > 計算機配置 > 管理模板>系統 >Device Guard (或者是:  裝置防護) > 啟用基於虛擬化的安全性。
 - 選擇已禁用。
 
 - 轉到" 控制面板" >" 解除安裝程式" >" 開啟或關閉Windows功能"以關閉Hyper-V。
 - 選擇不重啟。

通過命令關閉Hyper-V (控制面板關閉Hyper-V起不到決定性作用，要徹底關閉Hyper-V) 

 - 以管理員身份執行Windows Powershell (管理員) (Windows鍵 X)，執行下面命令並重啟電腦: `bcdedit /set hypervisorlaunchtype off`