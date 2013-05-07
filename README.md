supervisorctl stop s21_stream_infracam
supervisorctl stop s21_stream_instacam

# Check if stream is online
## justin.tv

	curl 'http://api.justin.tv/api/stream/list.json?channel=instacam' | grep instacam

## ustream
	
	curl http://api.ustream.tv/json/channel/s21-instacam/getValueOf/status | grep -q "live"
