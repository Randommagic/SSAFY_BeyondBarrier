��� ���� �� ���� ���ø����̼��� ������ �� �ֵ��� �ϴ� ���
======
1. SDB �� �̿��� �� root �������� ����
```
sdb root on
```

2. SDB �� �̿��� ����, Ȥ�� Device Manager �� �̿��Ѵ�.
```
sdb connect "device IP"

sdb connect 70.12.115.41
```

3. /usr/lib/systemd/system/ ��ο� service ���� ���� �� ����
```
vi /usr/lib/systemd/system/your-service.service

[Unit]
Description=Your Service
After=multi-user.target

[Service]
Type=simple
ExecStart=/opt/usr/apps/your-package-name/bin/your-service-binary
Restart=always

[Install]
WantedBy=multi-user.target

```

4. ���� ����
```
systemctl daemon-reload
systemctl enable your-service.service
systemctl start your-service.service
systemctl status your-service.service
```

�Ƹ� �� ���̴�.