.. _clusterdetails:

------------------------
HPoC Cluster Details
------------------------

Cluster Hardware Details
++++++++++++++++++++++++


**Für den Hosted PoC wurde ein System mit 4 Nodes in 2 Höheneinheiten reserviert:**

.. figure:: images/cluster3060g5a.png

.. note::
  Bedenken Sie bitte, dass diese Testumgebung zum nicht zwangsläufig  auf der neuesten Hardware basiert und das zum anderen auf Grund der Entfernung zum Lab-Datacenter entsprechende Latenzen auftreten können. Nichtsdestotrotz lassen sich mit dieser Umgebung die typischen Routineaufgaben bzgl. einer Nutanix-Cluster-Plattform mit einer ausgezeichneten User-Experience testen.

Infrastruktur IPs
+++++++++++++++++

.. list-table::
   :widths: 10 10 10 10
   :header-rows: 1

   * - Nodes
     - CVMs
     - Hypervisors
     - IPMI
   * - **Position A**
     - 10.38.176.29
     - 10.38.176.25
     - 10.38.176.33
   * - **Position B**
     - 10.38.176.30
     - 10.38.176.26
     - 10.38.176.34
   * - **Position C**
     - 10.38.176.31
     - 10.38.176.27
     - 10.38.176.35
   * - **Position D**
     - 10.38.176.32
     - 10.38.176.28
     - 10.38.176.36


.. list-table::
  :widths: 20 20
  :header-rows: 1

  * - Services
    - IP-Adressen
  * - **Cluster virtual IP**
    - 10.38.176.37
  * - **iSCSI Data Services IP**
    - 10.38.176.38
  * - **Prism Central**
    - 10.38.176.39
  * - **Active Directory**
    - 10.38.176.41


Zugangsdaten
++++++++++++

Die folgende Tabelle führt die standardmäßig hinterlegten Zugangsdaten für die Umgebung auf (falls andere zum Einsatz kommen sollten wird dies gesondert aufgeführt):

.. list-table::
  :widths: 20 20 10
  :header-rows: 1

  * - Name
    - Benutzername
    - Passwort
  * - **IPMI**
    - ADMIN
    - ADMIN
  * - **Prism Element Web**
    - admin
    - ntnx2NUIX!
  * - **Prism Element SSH**
    - nutanix
    - ntnx2NUIX!
  * - **Prism Central Web**
    - admin
    - ntnx2NUIX!
  * - **Prism Central SSH**
    - nutanix
    - nutanix/4u
  * - **NTNXLAB Domain**
    - NTNXLAB\\Administrator
    - nutanix/4u
  * - **CentOS VM Image**
    - root
    - nutanix/4u


Darüber hinaus besitzt der Cluster eine dedizierte Domain-Controller-VM, welche die Active-Directory-Services für die **NTNXLAB.local** Domain bereitstellt. Die Domain wurde mit den folgenden Nutzern und Gruppen vorkonfiguriert:

.. list-table::
  :widths: 20 20 10
  :header-rows: 1

  * - Gruppe
    - Benutzername(n)
    - Passwort
  * - **Administrators / Domain Admins**
    - Administrator
    - nutanix/4u
  * - **Bootcamp Users**
    - User01-User25
    - nutanix/4u
  * - **SSP Admins**
    - Adminuser01-Adminuser25
    - nutanix/4u
  * - **SSP Operators**
    - Operator01-Operator25
    - nutanix/4u
  * - **SSP Developers**
    - Devuser01-Devuser25
    - nutanix/4u
  * - **SSP Consumers**
    - Consumer01-Consumer25
    - nutanix/4u
  * - **SSP Custom**
    - Custom01-Custom25
    - nutanix/4u

Netzwerk
++++++++

Die folgenden virtuellen Netzwerke wurden wie folgt vorkonfiguriert:

.. list-table::
   :widths: 33 33 33
   :header-rows: 1

   * -
     - **Primäres** Netzwerk
     - **Sekundäres** Netzwerk
   * - **VLAN**
     - 0
     - 2053
   * - **Netzwerk IP Adresse**
     - 10.38.176.0
     - 10.38.176.128
   * - **Netzmaske**
     - 255.255.255.128 (/25)
     - 255.255.255.128 (/25)
   * - **Default Gateway**
     - 10.38.176.1
     - 10.38.176.129
   * - **IP Address Management (IPAM)**
     - Aktiviert
     - Aktiviert
   * - **DHCP Pool**
     - 10.38.176.50  - 125
     - 10.38.176.132 - 253
   * - **Domain**
     - NTNXLAB.local
     - NTNXLAB.local
   * - **DNS**
     - 10.38.176.41 (DC VM)
     - 10.38.176.41 (DC VM)
