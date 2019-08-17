listenAddr: '127.0.0.1:12345'
useMultiplePorts: false
proxies:
  - name: 'Burst-BHD'
    upstreams:
      - name: 'Burst Solo'
        mode: solo
        url: 'http://your-wallet-ip:8125'
        passphrases:
          'yourAccountId': 'your passphrase'
        targetDL: 86400
        weight: 10
      - name: 'BHD Solo'
        isBHD: true
        mode: solo
        url: 'http://user:pass@your-wallet-ip:8732'
        targetDL: 86400
        weight: 11