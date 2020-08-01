# heartbeat
heartbeat by cobe lee

heartbeat
The heartbeat timer

中文文档

Heartbeat introduction
Heartbeat is a response to the timing of multi-tasking callback based on Go

Installation
go get -u github.com/noaway/heartbeat
Heartbeat simple to use
Create task
name, spec := "12138", 5
ht, err := heartbeat.NewTast(name, spec)

if err != nil {
	fmt.Println(err)
}

// Run a new mission
ht.Start(func() error {
	//Call the callback every 5 seconds
	fmt.Println(name)
	return nil
})
More usage, please reference

heartbeat_test.go
