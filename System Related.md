# 1. what happend google?  
    
    1.type process, local machine
    interruption, for io
    local cache for searching recent result
    
    2. DNS find server IP
    
    3.http / https connections
    3 shake hands, TCP connection
    
    4. server connection
    7 tiers, seals each time
    application -> transport -> network -> data -> physical
    
    5. server end
    Single thread better, context switch lose cache
    
    6. render
    cookie for store data, also local persist
    
  
# 2. design a parking lot

    1.use case
    driver drives in -> get to the gate, arrange spot, take a ticket, gate open, car pass, gate close, park to the spot
    driver get out -> drive away from spot, get to the gate, pay money,release spot, gate open, car pass, gate close
    
    2.class definition
    - Entity Class:
    Driver, Parking slot, Ticket
    - Control Class
    Gate
    - Boundary Class
    Parking lot
    
    Driver:
    get_id, get_ticket, set_ticket, get_parkinglot, set_parkinglot
    
    Parking slot:
    get_id, get_driver, set_driver, get_opening
    
    Ticket:
    get_id, get_time, get_driver, get_price, get_parking slot
    
    Gate:
    get_id, get_condition, open, close, find(parkinglot), update_parkinglot, gen_ticket(price, parkinglot, driver)
    
    Boundary:
    parking lot
    -pq: all available lot, ordered by distance
    +getslot()
    +getgate()
    
# 3. Design Tiny Url
    Senario: long -> short, short -> long
    N
    Application: long -> hash -> dic -> short
                 short -> dic -> long
                 trade off?
    Kilobit: calculation
    Evolve: distributed system

# 4. design file system
    
