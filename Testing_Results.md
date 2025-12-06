# Testing & Validation Results

## 1. Connectivity Tests
- [ ] Ping between HQ VLANs
- [ ] Ping from Branch → HQ
- [ ] Ping from users → DMZ servers

## 2. DHCP Tests
- [ ] IP assigned correctly in each VLAN
- [ ] Default gateway & DNS options correct

## 3. Security & VPN
- [ ] IPsec VPN tunnel up
- [ ] Internet access through FortiGate
- [ ] Policies applied as expected (allow/deny)

## 4. High Availability
- [ ] FortiGate HA failover tested
- [ ] No packet loss during failover (or minimal)

## 5. ISE Authentication
- [ ] User authenticated via 802.1X / RADIUS
- [ ] TACACS+ device admin working
