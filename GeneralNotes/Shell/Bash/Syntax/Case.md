```bash
case <variable> in
	<pattern1>)
		<command>
		;;
	<pattern2>)
		<command>
		;;
esac
```

A default can be implemented with a wildcard regex e.g.
```bash
case <variable> in
	*)
		<command>
		;;
esac
```